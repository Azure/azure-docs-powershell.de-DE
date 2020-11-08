---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: 82b5bdd7e10b8119a058ab3a30f6836ff9255d01
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178024"
---
# <span data-ttu-id="ecd56-101">Get-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="ecd56-101">Get-AzHpcCache</span></span>

## <span data-ttu-id="ecd56-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ecd56-102">SYNOPSIS</span></span>
<span data-ttu-id="ecd56-103">Ruft einen Cache (s) ab.</span><span class="sxs-lookup"><span data-stu-id="ecd56-103">Gets a cache(s).</span></span>

## <span data-ttu-id="ecd56-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecd56-104">SYNTAX</span></span>

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ecd56-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ecd56-105">DESCRIPTION</span></span>
<span data-ttu-id="ecd56-106">Das Cmdlet " **Get-AzHpcCache** " Ruft einen einzelnen Cache, Cache (s) in einer bestimmten Ressourcengruppe oder eine Abonnement weite Liste von Caches ab.</span><span class="sxs-lookup"><span data-stu-id="ecd56-106">The **Get-AzHpcCache** cmdlet gets a single cache, cache(s) in a specific resource group, or subscription wide list of caches.</span></span>

## <span data-ttu-id="ecd56-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ecd56-107">EXAMPLES</span></span>

### <span data-ttu-id="ecd56-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ecd56-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### <span data-ttu-id="ecd56-109">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ecd56-109">Example 2</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### <span data-ttu-id="ecd56-110">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ecd56-110">Example 3</span></span>
```powershell
PS C:\> Get-AzHPCCache
```

## <span data-ttu-id="ecd56-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ecd56-111">PARAMETERS</span></span>

### <span data-ttu-id="ecd56-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecd56-112">-DefaultProfile</span></span>
<span data-ttu-id="ecd56-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ecd56-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecd56-114">-Name</span><span class="sxs-lookup"><span data-stu-id="ecd56-114">-Name</span></span>
<span data-ttu-id="ecd56-115">Name des bestimmten Caches.</span><span class="sxs-lookup"><span data-stu-id="ecd56-115">Name of specific cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd56-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecd56-116">-ResourceGroupName</span></span>
<span data-ttu-id="ecd56-117">Name der Ressourcengruppe, unter der Sie den Cache (s) auflisten möchten.</span><span class="sxs-lookup"><span data-stu-id="ecd56-117">Name of resource group under which you want to list cache(s).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd56-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecd56-118">CommonParameters</span></span>
<span data-ttu-id="ecd56-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecd56-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecd56-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecd56-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecd56-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ecd56-121">INPUTS</span></span>

### <span data-ttu-id="ecd56-122">System. String</span><span class="sxs-lookup"><span data-stu-id="ecd56-122">System.String</span></span>

## <span data-ttu-id="ecd56-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ecd56-123">OUTPUTS</span></span>

### <span data-ttu-id="ecd56-124">Microsoft. Azure. PowerShell. Cmdlets. HPCCache. Models. PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="ecd56-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="ecd56-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="ecd56-125">NOTES</span></span>

## <span data-ttu-id="ecd56-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ecd56-126">RELATED LINKS</span></span>
