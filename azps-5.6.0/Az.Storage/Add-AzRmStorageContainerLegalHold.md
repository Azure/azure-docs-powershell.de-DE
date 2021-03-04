---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/add-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 8b0608a350f73de4280380abf7fd213d48742022
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930712"
---
# <span data-ttu-id="e23ab-101">Add-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="e23ab-101">Add-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="e23ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e23ab-102">SYNOPSIS</span></span>
<span data-ttu-id="e23ab-103">Fügt einem Speicherblobcontainer juristische Haltetags hinzu.</span><span class="sxs-lookup"><span data-stu-id="e23ab-103">Adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="e23ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e23ab-104">SYNTAX</span></span>

### <span data-ttu-id="e23ab-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e23ab-105">AccountName (Default)</span></span>
```
Add-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e23ab-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e23ab-106">AccountObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e23ab-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="e23ab-107">ContainerObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e23ab-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e23ab-108">DESCRIPTION</span></span>
<span data-ttu-id="e23ab-109">Das **Add-AzRmStorageContainerLegalHold-Cmdlet** fügt einem Speicherblobcontainer juristische Haltetags hinzu.</span><span class="sxs-lookup"><span data-stu-id="e23ab-109">The **Add-AzRmStorageContainerLegalHold** cmdlet adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="e23ab-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e23ab-110">EXAMPLES</span></span>

### <span data-ttu-id="e23ab-111">Beispiel 1: Hinzufügen von rechtlichen Haltetags zu einem Speicherblobcontainer mit dem Namen des Speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="e23ab-111">Example 1: Add legal hold tags to a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Add-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2
```

<span data-ttu-id="e23ab-112">Mit diesem Befehl werden einem Speicherblobcontainer mit dem Namen des Speicherkontos und dem Containernamen juristische Haltetags hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="e23ab-112">This command adds legal hold tags to a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="e23ab-113">Beispiel 2: Hinzufügen von Legal Hold-Tags zu einem Speicherblobcontainer mit Speicherkontoobjekt und Containername</span><span class="sxs-lookup"><span data-stu-id="e23ab-113">Example 2: Add legal hold tags to a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

<span data-ttu-id="e23ab-114">Mit diesem Befehl werden einem Speicherblobcontainer mit Speicherkontoobjekt und Containername juristische Haltetags hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="e23ab-114">This command adds legal hold tags to a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="e23ab-115">Beispiel 3: Hinzufügen von Legal Hold-Tags zu allen Speicherblobcontainern in einem Speicherkonto mit Pipeline</span><span class="sxs-lookup"><span data-stu-id="e23ab-115">Example 3: Add legal hold tags to all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

<span data-ttu-id="e23ab-116">Mit diesem Befehl werden allen Speicherblobcontainern in einem Speicherkonto mit Pipeline legale Haltetags hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="e23ab-116">This command adds legal hold tags to all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="e23ab-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e23ab-117">PARAMETERS</span></span>

### <span data-ttu-id="e23ab-118">-Container</span><span class="sxs-lookup"><span data-stu-id="e23ab-118">-Container</span></span>
<span data-ttu-id="e23ab-119">Speichercontainerobjekt</span><span class="sxs-lookup"><span data-stu-id="e23ab-119">Storage container object</span></span>

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

### <span data-ttu-id="e23ab-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e23ab-120">-DefaultProfile</span></span>
<span data-ttu-id="e23ab-121">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e23ab-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e23ab-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e23ab-122">-Name</span></span>
<span data-ttu-id="e23ab-123">Containername</span><span class="sxs-lookup"><span data-stu-id="e23ab-123">Container Name</span></span>

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

### <span data-ttu-id="e23ab-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e23ab-124">-ResourceGroupName</span></span>
<span data-ttu-id="e23ab-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="e23ab-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="e23ab-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e23ab-126">-StorageAccount</span></span>
<span data-ttu-id="e23ab-127">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="e23ab-127">Storage account object</span></span>

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

### <span data-ttu-id="e23ab-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e23ab-128">-StorageAccountName</span></span>
<span data-ttu-id="e23ab-129">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="e23ab-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="e23ab-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="e23ab-130">-Tag</span></span>
<span data-ttu-id="e23ab-131">Container LegalHold-Tags</span><span class="sxs-lookup"><span data-stu-id="e23ab-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="e23ab-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e23ab-132">-Confirm</span></span>
<span data-ttu-id="e23ab-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e23ab-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e23ab-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e23ab-134">-WhatIf</span></span>
<span data-ttu-id="e23ab-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e23ab-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e23ab-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e23ab-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e23ab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e23ab-137">CommonParameters</span></span>
<span data-ttu-id="e23ab-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e23ab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e23ab-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e23ab-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e23ab-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e23ab-140">INPUTS</span></span>

### <span data-ttu-id="e23ab-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e23ab-141">System.String</span></span>

### <span data-ttu-id="e23ab-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e23ab-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="e23ab-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="e23ab-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="e23ab-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e23ab-144">OUTPUTS</span></span>

### <span data-ttu-id="e23ab-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="e23ab-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="e23ab-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e23ab-146">NOTES</span></span>

## <span data-ttu-id="e23ab-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e23ab-147">RELATED LINKS</span></span>
