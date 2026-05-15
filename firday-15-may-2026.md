---
type: Activity
Status: Active
product: APS
Date: 2026-05-13
---
# Firday, 15 May 2026

## Based on Timeline

- [ ] Development data backup management to sharepoint
- [x] Solved issue when export leads

```php
$leads = DB::table('report_leads')
    ->select($headers)
    ->where('isActive', 'Yes')
    ->when($findUser, function ($query) use ($findUser) {
        if ($findUser->project) {
            return $query->where('projectName', $findUser->project->name);
        }
        return $query;
    })
    ->when($type, function ($query) use ($type, $month) {
        if ($type == 'mtd') {
            return $query->whereYear('createdDate', date('Y'))
                ->whereMonth('createdDate', $month);
        } else if ($type == 'ytd') {
            $startOfYear = Carbon::now()->startOfYear();
            $endOfMonth = Carbon::createFromDate(now()->year, $month, 1)->endOfMonth();
            return $query->whereBetween('createdDate', [$startOfYear, $endOfMonth]);
        }
        return $query;
    })
    ->when(!$type, function ($query) use ($type) {
        return $query->whereDate('createdDate', '>', now()->subDays(60));
    });
```

*

## Additional REST Revamp
