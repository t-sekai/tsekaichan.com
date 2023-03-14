---
title: I/O
weight: 30
menu:
  notes:
    name: I/O
    identifier: notes-java-basics-io
    parent: notes-java-basics
    weight: 30
---

<!-- Scanner -->
{{< note title="Scanner">}}

```java
Scanner sc = new Scanner(System.in);
int n = sc.nextInt();
long ln = sc.nextLong();
double dn = sc.nextDouble();
String s = sc.read(); //sc.readLine();
```

{{< /note >}}

<!-- BufferedReader -->

{{< note title="BufferedReader" >}}

```java
BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
int n = Integer.parseInt(br.readLine());
int a[] = new int[n];
//n elements in one line
StringTokenizer st = new StringTokenizer(br.readLine());
for(int i = 0; i < n; ++i){
  a[i] = Integer.parseInt(st.nextToken());
}
```

{{< /note >}}

<!-- StreamTokenizer -->

{{< note title="StreamTokenizer" >}}

```java
private static StreamTokenizer st;
private static int nextInt() throws IOException{
  st.nextToken();
  return (int)st.nval;
}
private static long nextLong() throws IOException{
  st.nextToken();
  return (long)st.nval;
}
private static double nextDouble() throws IOException{
  st.nextToken();
  return st.nval;
}
private static String read() throws IOException{ //don't recommend to read string with this i/o
  st.nextToken();
  return st.sval;
}
public static void main(String[] args){
  st = new StreamTokenizer(new BufferedReader(new InputStreamReader(System.in)));
  int n = nextInt();
  long ln = nextLong();
  double dn = nextDouble();
  String s = read();
}
```

{{< /note >}}

<!-- PrintWriter -->

{{< note title="PrintWriter" >}}

```java
PrintWriter pw = new PrintWriter(new BufferedWriter(new OutputStreamWriter(System.out)));
pw.println("Hello world!");
pw.close();
```

{{< /note >}}