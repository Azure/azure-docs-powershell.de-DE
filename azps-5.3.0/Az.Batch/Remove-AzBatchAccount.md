---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
ms.openlocfilehash: ae67aac391f2cce2a37be8a5a15a0fd0ea37cdd9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471131"
---
# <span data-ttu-id="be91f-101">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="be91f-101">Remove-AzBatchAccount</span></span>

## <span data-ttu-id="be91f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be91f-102">SYNOPSIS</span></span>
<span data-ttu-id="be91f-103">Entfernt ein Batchkonto.</span><span class="sxs-lookup"><span data-stu-id="be91f-103">Removes a Batch account.</span></span>

## <span data-ttu-id="be91f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be91f-104">SYNTAX</span></span>

```
Remove-AzBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be91f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be91f-105">DESCRIPTION</span></span>
<span data-ttu-id="be91f-106">Das **Cmdlet "Remove-AzBatchAccount"** entfernt ein Azure Batch-Konto.</span><span class="sxs-lookup"><span data-stu-id="be91f-106">The **Remove-AzBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="be91f-107">Dieses Cmdlet fordert Sie vor dem Entfernen eines Kontos auf, es sei denn, Sie geben den Parameter *"Force"* an.</span><span class="sxs-lookup"><span data-stu-id="be91f-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="be91f-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="be91f-108">EXAMPLES</span></span>

### <span data-ttu-id="be91f-109">Beispiel 1: Entfernen eines Batchkontos</span><span class="sxs-lookup"><span data-stu-id="be91f-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="be91f-110">Mit diesem Befehl wird das Batchkonto namens "pfuller" entfernt.</span><span class="sxs-lookup"><span data-stu-id="be91f-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="be91f-111">Dieser Befehl fordert Sie zur Bestätigung auf, bevor das Konto gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="be91f-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="be91f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be91f-112">PARAMETERS</span></span>

### <span data-ttu-id="be91f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="be91f-113">-AccountName</span></span>
<span data-ttu-id="be91f-114">Gibt den Namen des Batchkontos an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="be91f-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="be91f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be91f-115">-DefaultProfile</span></span>
<span data-ttu-id="be91f-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be91f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be91f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="be91f-117">-Force</span></span>
<span data-ttu-id="be91f-118">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="be91f-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="be91f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be91f-119">-ResourceGroupName</span></span>
<span data-ttu-id="be91f-120">Gibt die Ressourcengruppe des Kontos an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="be91f-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="be91f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be91f-121">-Confirm</span></span>
<span data-ttu-id="be91f-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="be91f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be91f-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="be91f-123">-WhatIf</span></span>
<span data-ttu-id="be91f-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="be91f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be91f-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="be91f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be91f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be91f-126">CommonParameters</span></span>
<span data-ttu-id="be91f-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be91f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be91f-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be91f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be91f-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="be91f-129">INPUTS</span></span>

### <span data-ttu-id="be91f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="be91f-130">System.String</span></span>

## <span data-ttu-id="be91f-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="be91f-131">OUTPUTS</span></span>

### <span data-ttu-id="be91f-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="be91f-132">System.Void</span></span>

## <span data-ttu-id="be91f-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="be91f-133">NOTES</span></span>

## <span data-ttu-id="be91f-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="be91f-134">RELATED LINKS</span></span>

[<span data-ttu-id="be91f-135">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="be91f-135">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="be91f-136">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="be91f-136">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="be91f-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="be91f-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="be91f-138">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="be91f-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
