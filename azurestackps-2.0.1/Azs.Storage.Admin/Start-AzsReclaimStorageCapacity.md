---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/start-azsreclaimstoragecapacity
schema: 2.0.0
ms.openlocfilehash: bb2eecb93a7a18559dc6fbe58cd5f07c737e16b5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005361"
---
# <span data-ttu-id="440bc-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="440bc-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="440bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="440bc-102">SYNOPSIS</span></span>


## <span data-ttu-id="440bc-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="440bc-103">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="440bc-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="440bc-104">DESCRIPTION</span></span>


## <span data-ttu-id="440bc-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="440bc-105">EXAMPLES</span></span>

### <span data-ttu-id="440bc-106">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="440bc-106">Example 1:</span></span>
```powershell
PS C:\> Start-AzsReclaimStorageCapacity
```

<span data-ttu-id="440bc-107">Starten Sie die Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="440bc-107">Start garbage collection.</span></span>

## <span data-ttu-id="440bc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="440bc-108">PARAMETERS</span></span>

### <span data-ttu-id="440bc-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="440bc-109">-AsJob</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="440bc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="440bc-110">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="440bc-111">-Force</span><span class="sxs-lookup"><span data-stu-id="440bc-111">-Force</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="440bc-112">-Standort</span><span class="sxs-lookup"><span data-stu-id="440bc-112">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="440bc-113">-Nowait</span><span class="sxs-lookup"><span data-stu-id="440bc-113">-NoWait</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="440bc-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="440bc-114">-PassThru</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="440bc-115">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="440bc-115">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="440bc-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="440bc-116">-Confirm</span></span>
<span data-ttu-id="440bc-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="440bc-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="440bc-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="440bc-118">-WhatIf</span></span>
<span data-ttu-id="440bc-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="440bc-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="440bc-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="440bc-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="440bc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="440bc-121">CommonParameters</span></span>
<span data-ttu-id="440bc-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="440bc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="440bc-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="440bc-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="440bc-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="440bc-124">INPUTS</span></span>

## <span data-ttu-id="440bc-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="440bc-125">OUTPUTS</span></span>

### <span data-ttu-id="440bc-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="440bc-126">System.Boolean</span></span>



## <span data-ttu-id="440bc-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="440bc-127">NOTES</span></span>

## <span data-ttu-id="440bc-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="440bc-128">RELATED LINKS</span></span>

