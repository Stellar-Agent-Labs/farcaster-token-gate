# Triarchy Token Gate Frame

This is a Farcaster Frame built with [Frog.fm](https://frog.fm), [Next.js](https://nextjs.org/), [Viem](https://viem.sh), and [Neynar SDK](https://neynar.com/).
It implements an ERC20 Token Gate, meaning a user can only interact with the frame if they hold a specific asset on-chain.

## Features
- **Neynar Bulk User API**: Safely resolves FID to connected Ethereum Addresses.
- **Viem Multicall Optimization**: Reads `balanceOf` across multiple connected custody addresses in a single `multicall` RPC request, vastly reducing latency.
- **Dynamic Failsafe**: Built-in edge-case catching (Dev Mode without keys).

## Deployment Instruction (Vercel)
This repository is optimized for Edge Networks. To deploy:
1. Import this repository into Vercel.
2. Set the Environment Variables:
   - `NEYNAR_API_KEY`: Your Neynar API Key.
   - `RPC_URL`: (Optional) Base/Mainnet RPC URL.
   - `NEXT_PUBLIC_SITE_URL`: The production URL (e.g. `https://my-frame.vercel.app`).
3. Deploy!

## Frameworks
- Next.js 14 App Router
- Frog `0.15`
- Viem
- TailwindCSS
