---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: eedeeb3311373c240cd564534d3438b948c7a0f6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304056"
---
# <span data-ttu-id="6593f-101">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6593f-101">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="6593f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6593f-102">SYNOPSIS</span></span>
<span data-ttu-id="6593f-103">Entfernt "ImmutabilityPolicy" eines Speicher-BLOB-Containers mit einer nicht gesperrten Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="6593f-103">Removes ImmutabilityPolicy of a Storage blob container with an unlocked policy</span></span>

## <span data-ttu-id="6593f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6593f-104">SYNTAX</span></span>

### <span data-ttu-id="6593f-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6593f-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6593f-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="6593f-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6593f-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="6593f-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6593f-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="6593f-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6593f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6593f-109">DESCRIPTION</span></span>
<span data-ttu-id="6593f-110">Das **Cmdlet "Remove-AzRmStorageContainerImmutabilityPolicy"** entfernt "ImmutabilityPolicy" eines Speicher-BLOB-Containers mit einer nicht gesperrten Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="6593f-110">The **Remove-AzRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob container with an unlocked policy.</span></span>

## <span data-ttu-id="6593f-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6593f-111">EXAMPLES</span></span>

### <span data-ttu-id="6593f-112">Beispiel 1: Entfernen entsperrter ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Namen des Speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="6593f-112">Example 1: Remove unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="6593f-113">Mit diesem Befehl wird die entsperrte ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Namen des Speicherkontos und dem Containernamen entfernt.</span><span class="sxs-lookup"><span data-stu-id="6593f-113">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="6593f-114">Beispiel 2: Entfernen entsperrter ImmutabilityPolicy eines Speicher-BLOB-Containers mit Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="6593f-114">Example 2: Remove unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="6593f-115">Mit diesem Befehl wird die entsperrte ImmutabilityPolicy eines Speicher-BLOB-Containers mit Speicherkontoobjekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="6593f-115">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="6593f-116">Beispiel 3: Entfernen von entsperrter ImmutabilityPolicy eines Speicher-BLOB-Containers mit Containerobjekt</span><span class="sxs-lookup"><span data-stu-id="6593f-116">Example 3: Remove unlocked ImmutabilityPolicy of a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="6593f-117">Mit diesem Befehl wird die entsperrte ImmutabilityPolicy eines Speicher-BLOB-Containers mit Einem Speichercontainerobjekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="6593f-117">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="6593f-118">Beispiel 4: Entfernen von entsperrter ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem ImmutabilityPolicy-Objekt</span><span class="sxs-lookup"><span data-stu-id="6593f-118">Example 4: Remove unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="6593f-119">Mit diesem Befehl wird die entsperrte ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem ImmutabilityPolicy-Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="6593f-119">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="6593f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6593f-120">PARAMETERS</span></span>

### <span data-ttu-id="6593f-121">-Container</span><span class="sxs-lookup"><span data-stu-id="6593f-121">-Container</span></span>
<span data-ttu-id="6593f-122">Speichercontainerobjekt</span><span class="sxs-lookup"><span data-stu-id="6593f-122">Storage container object</span></span>

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

### <span data-ttu-id="6593f-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="6593f-123">-ContainerName</span></span>
<span data-ttu-id="6593f-124">Containername</span><span class="sxs-lookup"><span data-stu-id="6593f-124">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6593f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6593f-125">-DefaultProfile</span></span>
<span data-ttu-id="6593f-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6593f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6593f-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="6593f-127">-Etag</span></span>
<span data-ttu-id="6593f-128">E-Tag der Immutbarkeitsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="6593f-128">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6593f-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6593f-129">-InputObject</span></span>
<span data-ttu-id="6593f-130">Zu entfernende ImmutabilityPolicy-Objekt entsperrt</span><span class="sxs-lookup"><span data-stu-id="6593f-130">Unlocked ImmutabilityPolicy Object to Remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6593f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6593f-131">-ResourceGroupName</span></span>
<span data-ttu-id="6593f-132">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="6593f-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="6593f-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6593f-133">-StorageAccount</span></span>
<span data-ttu-id="6593f-134">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="6593f-134">Storage account object</span></span>

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

### <span data-ttu-id="6593f-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6593f-135">-StorageAccountName</span></span>
<span data-ttu-id="6593f-136">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="6593f-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="6593f-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6593f-137">-Confirm</span></span>
<span data-ttu-id="6593f-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6593f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6593f-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6593f-139">-WhatIf</span></span>
<span data-ttu-id="6593f-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6593f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6593f-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6593f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6593f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6593f-142">CommonParameters</span></span>
<span data-ttu-id="6593f-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6593f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6593f-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6593f-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6593f-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6593f-145">INPUTS</span></span>

### <span data-ttu-id="6593f-146">System.String</span><span class="sxs-lookup"><span data-stu-id="6593f-146">System.String</span></span>

### <span data-ttu-id="6593f-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6593f-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="6593f-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="6593f-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="6593f-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6593f-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="6593f-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6593f-150">OUTPUTS</span></span>

### <span data-ttu-id="6593f-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6593f-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="6593f-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6593f-152">NOTES</span></span>

## <span data-ttu-id="6593f-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6593f-153">RELATED LINKS</span></span>
