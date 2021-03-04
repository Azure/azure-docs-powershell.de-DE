---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 9788acb95be63d9e76525cbeaf7904cd260baae0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937272"
---
# <span data-ttu-id="b855c-101">Remove-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="b855c-101">Remove-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="b855c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b855c-102">SYNOPSIS</span></span>
<span data-ttu-id="b855c-103">Entfernt juristische Aufbewahrungstags aus einem Speicherblobcontainer</span><span class="sxs-lookup"><span data-stu-id="b855c-103">Removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="b855c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b855c-104">SYNTAX</span></span>

### <span data-ttu-id="b855c-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b855c-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b855c-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b855c-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b855c-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="b855c-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b855c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b855c-108">DESCRIPTION</span></span>
<span data-ttu-id="b855c-109">Das **Cmdlet Remove-AzRmStorageContainerLegalHold** entfernt juristische Haltetags aus einem Speicherblobcontainer.</span><span class="sxs-lookup"><span data-stu-id="b855c-109">The **Remove-AzRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="b855c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b855c-110">EXAMPLES</span></span>

### <span data-ttu-id="b855c-111">Beispiel 1: Entfernen von Rechtlichen Haltetags aus einem Speicherblobcontainer mit Dem Namen des Speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="b855c-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="b855c-112">Mit diesem Befehl werden juristische Aufbewahrungstags aus einem Speicherblobcontainer mit dem Namen des Speicherkontos und dem Containernamen entfernt.</span><span class="sxs-lookup"><span data-stu-id="b855c-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="b855c-113">Beispiel 2: Entfernen von Rechtlichen Haltetags aus einem Speicherblobcontainer mit Speicherkontoobjekt und Containername</span><span class="sxs-lookup"><span data-stu-id="b855c-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2
```

<span data-ttu-id="b855c-114">Mit diesem Befehl werden juristische Haltetags aus einem Speicherblobcontainer mit Speicherkontoobjekt und Containername entfernt.</span><span class="sxs-lookup"><span data-stu-id="b855c-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="b855c-115">Beispiel 3: Entfernen von rechtlichen Haltetags aus allen Speicherblobcontainern in einem Speicherkonto mit Pipeline</span><span class="sxs-lookup"><span data-stu-id="b855c-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="b855c-116">Mit diesem Befehl werden juristische Haltetags aus allen Speicherblobcontainern in einem Speicherkonto mit Pipeline entfernt.</span><span class="sxs-lookup"><span data-stu-id="b855c-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="b855c-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b855c-117">PARAMETERS</span></span>

### <span data-ttu-id="b855c-118">-Container</span><span class="sxs-lookup"><span data-stu-id="b855c-118">-Container</span></span>
<span data-ttu-id="b855c-119">Speichercontainerobjekt</span><span class="sxs-lookup"><span data-stu-id="b855c-119">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b855c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b855c-120">-DefaultProfile</span></span>
<span data-ttu-id="b855c-121">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b855c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b855c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b855c-122">-Name</span></span>
<span data-ttu-id="b855c-123">Containername</span><span class="sxs-lookup"><span data-stu-id="b855c-123">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b855c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b855c-124">-ResourceGroupName</span></span>
<span data-ttu-id="b855c-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="b855c-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b855c-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b855c-126">-StorageAccount</span></span>
<span data-ttu-id="b855c-127">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="b855c-127">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b855c-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b855c-128">-StorageAccountName</span></span>
<span data-ttu-id="b855c-129">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="b855c-129">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b855c-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="b855c-130">-Tag</span></span>
<span data-ttu-id="b855c-131">Container LegalHold-Tags</span><span class="sxs-lookup"><span data-stu-id="b855c-131">Container LegalHold Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b855c-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b855c-132">-Confirm</span></span>
<span data-ttu-id="b855c-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b855c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b855c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b855c-134">-WhatIf</span></span>
<span data-ttu-id="b855c-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b855c-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b855c-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b855c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b855c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b855c-137">CommonParameters</span></span>
<span data-ttu-id="b855c-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b855c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b855c-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b855c-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b855c-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b855c-140">INPUTS</span></span>

### <span data-ttu-id="b855c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b855c-141">System.String</span></span>

### <span data-ttu-id="b855c-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b855c-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="b855c-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="b855c-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="b855c-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b855c-144">OUTPUTS</span></span>

### <span data-ttu-id="b855c-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="b855c-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="b855c-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b855c-146">NOTES</span></span>

## <span data-ttu-id="b855c-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b855c-147">RELATED LINKS</span></span>
