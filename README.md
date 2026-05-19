<div align="center">

<!-- ANIMATED HEADER — replace the URL below with your own typing SVG from readme-typing-svg.demolab.com -->
[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&duration=3000&pause=1000&color=00D9FF&center=true&vCenter=true&width=600&lines=Hey%2C+I'm+davgonca+%F0%9F%91%8B;42+School+Student+%F0%9F%8F%AB;C+Developer+%F0%9F%92%BB;Always+learning%2C+always+building+%F0%9F%9A%80)](https://git.io/typing-svg)

<br/>

<!-- PROFILE VIEWS + FOLLOWERS BADGES -->
![Profile Views](https://komarev.com/ghpvc/?username=davgonca&color=00d9ff&style=flat-square&label=Profile+Views)
[![GitHub followers](https://img.shields.io/github/followers/davgonca?style=flat-square&color=00d9ff&labelColor=0d1117)](https://github.com/davgonca)

</div>

---

## 👤 About Me

```c
/* ************************************************************************** */
/*                                                                            */
/*   davgonca.h                                          42 Lisboa            */
/*                                                                            */
/* ************************************************************************** */

typedef struct s_developer {
    char    *name;        /* "David Gonçalves"        */
    char    *school;      /* "42 Lisboa"              */
    char    *focus;       /* "Low-level C / Systems"  */
    char    *status;      /* "Actively learning"      */
    bool    open_to_work; /* true                     */
}   t_developer;
```

> I'm a student at **42 Lisboa**, building strong foundations in systems programming through project-based learning. I enjoy understanding how things work under the hood — memory, file descriptors, and everything in between.

- 🏫 Currently at **42 Lisboa**
- 🔧 Focused on **C, systems programming, and Unix**
- 📚 Learning by doing — no lectures, only projects
- 🌍 Based in **Lisbon, Portugal**
- 💬 Ask me about anything C-related!

---

## 🏫 42 School

<div align="center">

| 🎓 Campus | 📍 Location | 🗓️ Started | 🌐 Network |
|:---------:|:-----------:|:----------:|:----------:|
| 42 Lisboa | Lisbon, PT  | 2026       | 42 Network |

</div>

**42** is a tuition-free, peer-to-peer coding school with no teachers and no lectures. Students learn entirely through projects, peer evaluations, and self-directed problem solving. Every project must pass rigorous automated tests and human code reviews.

> *"The only way to learn a new programming language is by writing programs in it."* — Dennis Ritchie

---

## 🚀 Projects

### ✅ Completed & Validated

---

#### 📚 `libft` — My C Standard Library

<div align="center">

![C](https://img.shields.io/badge/Language-C-blue?style=flat-square&logo=c&logoColor=white)
![Status](https://img.shields.io/badge/Status-Validated%20✓-brightgreen?style=flat-square)
![Score](https://img.shields.io/badge/Score-125%2F100-gold?style=flat-square)

</div>

> A complete re-implementation of the C standard library from scratch, plus bonus linked-list utilities.

**What it does:**
- Reimplements `string.h`, `stdlib.h`, and `ctype.h` functions
- Includes bonus linked-list functions (`ft_lstnew`, `ft_lstadd_back`, etc.)
- Serves as the foundation for all future 42 projects

**Concepts learned:**
- Manual memory management with `malloc` / `free`
- Pointer arithmetic and type casting
- Building and linking static libraries (`.a` files)
- Header files and include guards

**Key functions:**

```c
ft_strlen    ft_strcpy    ft_strjoin    ft_split
ft_atoi      ft_itoa      ft_memset     ft_calloc
ft_lstnew    ft_lstadd_back             ft_lstmap
```

**Example usage:**
```c
#include "libft.h"

int main(void)
{
    char *s = ft_strjoin("Hello, ", "World!");
    ft_putendl_fd(s, 1);   // → "Hello, World!"
    free(s);
    return (0);
}
```

---

#### 🖨️ `ft_printf` — Custom Printf

<div align="center">

![C](https://img.shields.io/badge/Language-C-blue?style=flat-square&logo=c&logoColor=white)
![Status](https://img.shields.io/badge/Status-Validated%20✓-brightgreen?style=flat-square)
![Score](https://img.shields.io/badge/Score-100%2F100-gold?style=flat-square)

</div>

> A reimplementation of the C `printf` function using variadic arguments.

**What it does:**
- Handles format specifiers: `%c`, `%s`, `%p`, `%d`, `%i`, `%u`, `%x`, `%X`, `%%`
- Processes variadic argument lists with `va_list`, `va_start`, `va_arg`, `va_end`
- Returns the total number of characters printed

**Concepts learned:**
- Variadic functions (`stdarg.h`)
- Format string parsing
- Recursive and iterative output strategies
- Handling edge cases (NULL pointers, negative numbers, hex conversion)

**Example usage:**
```c
#include "ft_printf.h"

int main(void)
{
    ft_printf("Name: %s | Age: %d | Hex: %x\n", "David", 21, 255);
    // → Name: David | Age: 21 | Hex: ff
    return (0);
}
```

---

#### 📄 `get_next_line` — Line-by-Line File Reader

<div align="center">

![C](https://img.shields.io/badge/Language-C-blue?style=flat-square&logo=c&logoColor=white)
![Status](https://img.shields.io/badge/Status-Validated%20✓-brightgreen?style=flat-square)
![Score](https://img.shields.io/badge/Score-125%2F100-gold?style=flat-square)

</div>

> Reads a file (or stdin) one line at a time using a single static buffer — no matter the `BUFFER_SIZE`.

**What it does:**
- Returns one line per call, including the trailing `\n`
- Works with any `BUFFER_SIZE` (1, 42, 9999...)
- Handles multiple file descriptors simultaneously (bonus)
- Returns `NULL` on EOF or error

**Concepts learned:**
- Static variables and persistent state between function calls
- File descriptors and the `read()` syscall
- Buffer management and stash/remainder patterns
- Memory safety and avoiding leaks across calls

**Example usage:**
```c
#include "get_next_line.h"
#include <fcntl.h>

int main(void)
{
    int     fd;
    char    *line;

    fd = open("file.txt", O_RDONLY);
    while ((line = get_next_line(fd)) != NULL)
    {
        ft_printf("%s", line);
        free(line);
    }
    close(fd);
    return (0);
}
```

---

### 🔮 Coming Soon

| Project | Description | Status |
|---------|-------------|--------|
| `push_swap` | Sort a stack using a limited set of operations | 🔄 In progress |
| `pipex` | Recreate shell pipe behaviour in C | ⏳ Upcoming |
| `so_long` | 2D game using MiniLibX | ⏳ Upcoming |
| `minitalk` | Process communication via UNIX signals | ⏳ Upcoming |
| `minishell` | Build a minimal Bash shell | 🎯 Goal |

---

## 🛠️ Skills & Technologies

<div align="center">

### Languages
![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
![Shell](https://img.shields.io/badge/Shell-121011?style=for-the-badge&logo=gnu-bash&logoColor=white)
![Markdown](https://img.shields.io/badge/Markdown-000000?style=for-the-badge&logo=markdown&logoColor=white)

### Tools & Environment
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Vim](https://img.shields.io/badge/Vim-019733?style=for-the-badge&logo=vim&logoColor=white)

### Concepts
![Memory Management](https://img.shields.io/badge/Memory%20Management-gray?style=for-the-badge)
![Pointers](https://img.shields.io/badge/Pointers%20%26%20References-gray?style=for-the-badge)
![File Descriptors](https://img.shields.io/badge/File%20Descriptors-gray?style=for-the-badge)
![Data Structures](https://img.shields.io/badge/Linked%20Lists-gray?style=for-the-badge)

</div>

---

## 📊 GitHub Stats

<div align="center">

<!-- STATS CARD: replace "davgonca" with your GitHub username -->
<img height="180em" src="https://github-readme-stats.vercel.app/api?username=davgonca&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true&hide_border=true"/>
<img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=davgonca&layout=compact&theme=tokyonight&hide_border=true&langs_count=6"/>

</div>

<div align="center">

<!-- STREAK STATS -->
<img src="https://github-readme-streak-stats.herokuapp.com/?user=davgonca&theme=tokyonight&hide_border=true" alt="GitHub Streak"/>

</div>

---

## 📬 Contact

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-davgonca-181717?style=for-the-badge&logo=github)](https://github.com/davgonca)
[![42 Intra](https://img.shields.io/badge/42%20Intra-davgonca-00BABC?style=for-the-badge&logo=42&logoColor=white)](https://profile.intra.42.fr/users/davgonca)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/YOUR_LINKEDIN)
[![Email](https://img.shields.io/badge/Email-Contact%20Me-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:YOUR_EMAIL@example.com)

</div>

---

<div align="center">

*"Programs must be written for people to read, and only incidentally for machines to execute."*
— Harold Abelson

<br/>

![Wave](https://capsule-render.vercel.app/api?type=waving&color=00d9ff&height=100&section=footer)

</div>
