import java.util.*;

class AlienDictionary {
  public static String findOrder(String[] words) {
    Map<Character, Set<Character>> graph = new HashMap<Character, Set<Character>>();
    Map<Character, Integer> counts = new HashMap<Character, Integer>();

    //PRASAANTH
    for(int i=1; i< words.length; i++)
    {
      String first = words[i-1];
      String second = words[i];
      
      int length = first.length() < second.length() ? first.length() :second.length();

      for(int j= 0; j<length;j++)
      {
         char parent = first.charAt(j);
         char child = second.charAt(j);

         if(parent == child) continue;
         
         Set<Character> set = null;
         if(graph.containsKey(parent))
           set = graph.get(parent);
         else
            set = new HashSet<Character>();

         set.add(child);
         graph.put(parent, set);

         if(counts.containsKey(child))
            counts.put(child, counts.get(child)+1);
         else
            counts.put(child, 1);
      }
    }
    return "";
  }

  public static void main(String[] args) {
    String result = AlienDictionary.findOrder(new String[] { "ba", "bc", "ac", "cab" });
    System.out.println("Character order: " + result);

    result = AlienDictionary.findOrder(new String[] { "cab", "aaa", "aab" });
    System.out.println("Character order: " + result);

    result = AlienDictionary.findOrder(new String[] { "ywx", "wz", "xww", "xz", "zyy", "zwz" });
    System.out.println("Character order: " + result);
  }
}
