## 1. Collection Interface
--Declaration--

Collection<DataType> obj = new ArrayList<>();

Example

Collection<Integer> numbers = new ArrayList<>();


--Common Methods--
obj.add(element);

obj.remove(element);

obj.size();

obj.isEmpty();

obj.clear();

obj.contains(element);

obj.iterator();

obj.toArray();

-- Example--

Collection<String> fruits = new ArrayList<>();

fruits.add("Apple");
fruits.add("Banana");

System.out.println(fruits);

fruits.remove("Apple");

System.out.println(fruits.size());

System.out.println(fruits.contains("Banana"));

fruits.clear();