---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/restore-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 81b6a6dc960e9364d6d3e54f6e6394e17559b7f8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007215"
---
# <span data-ttu-id="26891-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="26891-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="26891-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="26891-102">SYNOPSIS</span></span>


## <span data-ttu-id="26891-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="26891-103">SYNTAX</span></span>

```
Restore-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-NewAccountName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="26891-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26891-104">DESCRIPTION</span></span>


## <span data-ttu-id="26891-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="26891-105">EXAMPLES</span></span>

### <span data-ttu-id="26891-106">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="26891-106">Example 1:</span></span>
```powershell
PS C:\> Restore-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 
```

<span data-ttu-id="26891-107">Wiederherstellen eines gelöschten speicherkontos</span><span class="sxs-lookup"><span data-stu-id="26891-107">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="26891-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="26891-108">PARAMETERS</span></span>

### <span data-ttu-id="26891-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26891-109">-AsJob</span></span>


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

### <span data-ttu-id="26891-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26891-110">-DefaultProfile</span></span>


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

### <span data-ttu-id="26891-111">-Force</span><span class="sxs-lookup"><span data-stu-id="26891-111">-Force</span></span>


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

### <span data-ttu-id="26891-112">-Standort</span><span class="sxs-lookup"><span data-stu-id="26891-112">-Location</span></span>


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

### <span data-ttu-id="26891-113">-Name</span><span class="sxs-lookup"><span data-stu-id="26891-113">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="26891-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="26891-114">-NewAccountName</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="26891-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="26891-115">-NoWait</span></span>


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

### <span data-ttu-id="26891-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26891-116">-PassThru</span></span>


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

### <span data-ttu-id="26891-117">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="26891-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="26891-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="26891-118">-Confirm</span></span>
<span data-ttu-id="26891-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="26891-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26891-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26891-120">-WhatIf</span></span>
<span data-ttu-id="26891-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26891-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26891-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26891-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26891-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26891-123">CommonParameters</span></span>
<span data-ttu-id="26891-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26891-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26891-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26891-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26891-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="26891-126">INPUTS</span></span>

## <span data-ttu-id="26891-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="26891-127">OUTPUTS</span></span>

### <span data-ttu-id="26891-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26891-128">System.Boolean</span></span>



## <span data-ttu-id="26891-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="26891-129">NOTES</span></span>

## <span data-ttu-id="26891-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="26891-130">RELATED LINKS</span></span>

