import java.util.List;
import java.util.stream.Collectors;

public class StreamExample {
    public static void main(String[] args) {
        List<Integer> numbers = List.of(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);
        List<String> words = List.of("hello", "world", "java", "stream", "programming");

        List<Integer> evenNumbers = numbers.stream().filter(n -> n % 2 == 0).collect(Collectors.toList());
        List<String> upperCaseWords = words.stream().map(String::toUpperCase).collect(Collectors.toList());
        long count = words.stream().filter(word -> word.length() > 5).count();
        List<Integer> uniqueNumbers = numbers.stream().distinct().collect(Collectors.toList());

        System.out.println(evenNumbers);
        System.out.println(upperCaseWords);
        System.out.println(count);
        System.out.println(uniqueNumbers);
    }
}
