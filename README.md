# Return-the-top-key

````py
def solution(records): 
    # records  = []
    updated_records = {}
  
    for record in records: 
        a, b = record.split(':')
        b = int(b)
        updated_records[a] = updated_records.get(a,0) + b

    maxk, maxv = "", 0
    for a, b in updated_records.items(): 
        if b > maxv: 
            maxk, maxv = a, b 
    return maxk

records  = []
records.append("John: 22")
records.append("Mohn: 200")
records.append("John: 23")
records.append("Ron: 10")
print(solution(records))
````
