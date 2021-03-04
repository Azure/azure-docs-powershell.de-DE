---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
ms.openlocfilehash: 5b74f378bc867c1d39f27ebdd9972dfdda5457c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946336"
---
# <span data-ttu-id="49db6-101">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="49db6-101">Remove-AzBatchAccount</span></span>

## <span data-ttu-id="49db6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49db6-102">SYNOPSIS</span></span>
<span data-ttu-id="49db6-103">Entfernt ein Batchkonto.</span><span class="sxs-lookup"><span data-stu-id="49db6-103">Removes a Batch account.</span></span>

## <span data-ttu-id="49db6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49db6-104">SYNTAX</span></span>

```
Remove-AzBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49db6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49db6-105">DESCRIPTION</span></span>
<span data-ttu-id="49db6-106">Das **Cmdlet Remove-AzBatchAccount** entfernt ein Azure Batch-Konto.</span><span class="sxs-lookup"><span data-stu-id="49db6-106">The **Remove-AzBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="49db6-107">Dieses Cmdlet fordert Sie auf, bevor es ein Konto entfernt, es sei denn, Sie geben den Parameter *Erzwingen* an.</span><span class="sxs-lookup"><span data-stu-id="49db6-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="49db6-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="49db6-108">EXAMPLES</span></span>

### <span data-ttu-id="49db6-109">Beispiel 1: Entfernen eines Batchkontos</span><span class="sxs-lookup"><span data-stu-id="49db6-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="49db6-110">Mit diesem Befehl wird das Batchkonto mit dem Namen pfuller entfernt.</span><span class="sxs-lookup"><span data-stu-id="49db6-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="49db6-111">Dieser Befehl fordert Sie zur Bestätigung auf, bevor das Konto gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="49db6-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="49db6-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="49db6-112">PARAMETERS</span></span>

### <span data-ttu-id="49db6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="49db6-113">-AccountName</span></span>
<span data-ttu-id="49db6-114">Gibt den Namen des Batchkontos an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="49db6-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49db6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49db6-115">-DefaultProfile</span></span>
<span data-ttu-id="49db6-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49db6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49db6-117">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="49db6-117">-Force</span></span>
<span data-ttu-id="49db6-118">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="49db6-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="49db6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49db6-119">-ResourceGroupName</span></span>
<span data-ttu-id="49db6-120">Gibt die Ressourcengruppe des Kontos an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="49db6-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49db6-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="49db6-121">-Confirm</span></span>
<span data-ttu-id="49db6-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="49db6-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49db6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49db6-123">-WhatIf</span></span>
<span data-ttu-id="49db6-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49db6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49db6-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="49db6-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49db6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49db6-126">CommonParameters</span></span>
<span data-ttu-id="49db6-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49db6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49db6-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49db6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49db6-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="49db6-129">INPUTS</span></span>

### <span data-ttu-id="49db6-130">System.String</span><span class="sxs-lookup"><span data-stu-id="49db6-130">System.String</span></span>

## <span data-ttu-id="49db6-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="49db6-131">OUTPUTS</span></span>

### <span data-ttu-id="49db6-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="49db6-132">System.Void</span></span>

## <span data-ttu-id="49db6-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="49db6-133">NOTES</span></span>

## <span data-ttu-id="49db6-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="49db6-134">RELATED LINKS</span></span>

[<span data-ttu-id="49db6-135">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="49db6-135">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="49db6-136">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="49db6-136">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="49db6-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="49db6-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="49db6-138">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="49db6-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
