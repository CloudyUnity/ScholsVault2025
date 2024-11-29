
Remember:
	Language
		$L = \{f(x) | x \in \mathbb{A}\}$ 
	Regular Language
		$L_0 = \{a\}$ 
		$L_1 = L_0^*$
		$L_2 = L_0 \circ L_1$
		$L = L_3 \cup L_0$ 
	Grammar
		Context Free
			$\langle S \rangle \to x$
		Phase Structure
			$\langle S \rangle \to \langle A \rangle 0 \langle B \rangle$ 
			$\langle B \rangle \langle C \rangle \to haha$ 
		Regular (Left)
			$\langle S \rangle = b \langle B \rangle$
			$\langle B \rangle \to x$ 
			$\langle S \rangle \to \epsilon$ 
			Normal Form
				$\langle S \rangle \to b \langle B \rangle$ 
				$\langle S \rangle \to \epsilon$ 
	Regex
		$L = (\{a\} \circ \{b\})^* \cup \{c\}^*$ 
	FSA Transition Map
		$t(i, 0) = A$
		$t(A, 1) = A$ 
	Pumping Lemma
		$w = xuy$
		$xuy \in L \to xu^n y \in L$ 

It helps when doing FSA questions to think about what states are basically equivalent to each other
For example if the language is checking for an odd number of 0s in an even string
	Wrong approach:
		Try to account for every possible substring you can append onto the end of the string and still be valid
		Often these diagrams will look like a single acceptor state with many branches coming off it. BAD
	Correct approach:
		Think about the different states you can have:
			Odd 0s, Even 0s, Odd length, Even length
		This results in 4 states for each combination 
		Have a FSA that regularly enters invalid states and can only be accepted if it corrects itself