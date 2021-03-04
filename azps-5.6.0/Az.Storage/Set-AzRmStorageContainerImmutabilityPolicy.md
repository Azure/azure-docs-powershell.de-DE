---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 81db149500ce489801a25437fbb7a50443d7426a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929699"
---
# <span data-ttu-id="6f8aa-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6f8aa-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="6f8aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f8aa-102">SYNOPSIS</span></span>
<span data-ttu-id="6f8aa-103">Erstellt oder aktualisiert ImmutabilityPolicy eines Speicherblobcontainers</span><span class="sxs-lookup"><span data-stu-id="6f8aa-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="6f8aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f8aa-104">SYNTAX</span></span>

### <span data-ttu-id="6f8aa-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6f8aa-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f8aa-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="6f8aa-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f8aa-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="6f8aa-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f8aa-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="6f8aa-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f8aa-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="6f8aa-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f8aa-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="6f8aa-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f8aa-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="6f8aa-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f8aa-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="6f8aa-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f8aa-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f8aa-113">DESCRIPTION</span></span>
<span data-ttu-id="6f8aa-114">Das **Cmdlet Set-AzRmStorageContainerImmutabilityPolicy** erstellt oder aktualisiert ImmutabilityPolicy eines Speicherblobscontainers.</span><span class="sxs-lookup"><span data-stu-id="6f8aa-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="6f8aa-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6f8aa-115">EXAMPLES</span></span>

### <span data-ttu-id="6f8aa-116">Beispiel 1: Erstellen oder Aktualisieren von ImmutabilityPolicy eines Speicherblobcontainers mit Dem Namen des Speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="6f8aa-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="6f8aa-117">Mit diesem Befehl wird ImmutabilityPolicy eines Speicherblobcontainers mit dem Namen des Speicherkontos und dem Containernamen erstellt oder aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6f8aa-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="6f8aa-118">Beispiel 2: Erweitern der ImmutbarkeitPolicy eines Speicherblobcontainers mit Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="6f8aa-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="6f8aa-119">Mit diesem Befehl wird Die Immutbarkeitspolicy eines Speicherblobcontainers mit dem Speicherkontoobjekt erweitert.</span><span class="sxs-lookup"><span data-stu-id="6f8aa-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="6f8aa-120">ImmutabilityPolicy erweitern kann nur ausgeführt werden, nachdem ImmutabilityPolicy gesperrt wurde.</span><span class="sxs-lookup"><span data-stu-id="6f8aa-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="6f8aa-121">Beispiel 3: Aktualisieren der UnveränderlichkeitPolicy eines Speicherblobcontainers</span><span class="sxs-lookup"><span data-stu-id="6f8aa-121">Example 3: Update ImmutabilityPolicy of a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -AllowProtectedAppendWrite $true
```

<span data-ttu-id="6f8aa-122">Mit diesem Befehl wird ImmutabilityPolicy eines Speicher-Blob-Containers mit Speichercontainerobjekt dreimal aktualisiert: Zuerst auf ImmutabilityPeriod 12 Tage ohne etag, dann auf ImmutabilityPeriod 9 Tage mit etag, schließlich AllowProtectedAppendWrite aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6f8aa-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 3 times: First to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag, finally enabled AllowProtectedAppendWrite.</span></span>

### <span data-ttu-id="6f8aa-123">Beispiel 4: Erweitern der ImmutabilityPolicy eines Speicherblobcontainers mit dem ImmutabilityPolicy-Objekt</span><span class="sxs-lookup"><span data-stu-id="6f8aa-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="6f8aa-124">Mit diesem Befehl wird ImmutabilityPolicy eines Speicherblobcontainers mit dem ImmutabilityPolicy-Objekt erweitert.</span><span class="sxs-lookup"><span data-stu-id="6f8aa-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="6f8aa-125">ImmutabilityPolicy erweitern kann nur ausgeführt werden, nachdem ImmutabilityPolicy gesperrt wurde.</span><span class="sxs-lookup"><span data-stu-id="6f8aa-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="6f8aa-126">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6f8aa-126">PARAMETERS</span></span>

### <span data-ttu-id="6f8aa-127">-AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="6f8aa-127">-AllowProtectedAppendWrite</span></span>
<span data-ttu-id="6f8aa-128">Diese Eigenschaft kann nur für nicht gesperrte zeitbasierte Aufbewahrungsrichtlinien geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6f8aa-128">This property can only be changed for unlocked time-based retention policies.</span></span> <span data-ttu-id="6f8aa-129">Wenn diese Eigenschaft aktiviert ist, können neue Blöcke in einen Anfügeblob geschrieben werden, während der Schutz und die Compliance der Unveränderbarkeit beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="6f8aa-129">With this property enabled, new blocks can be written to an append blob while maintaining immutability protection and compliance.</span></span> <span data-ttu-id="6f8aa-130">Es können nur neue Blöcke hinzugefügt und vorhandene Blöcke nicht geändert oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="6f8aa-130">Only new blocks can be added and any existing blocks cannot be modified or deleted.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8aa-131">-Container</span><span class="sxs-lookup"><span data-stu-id="6f8aa-131">-Container</span></span>
<span data-ttu-id="6f8aa-132">Speichercontainerobjekt</span><span class="sxs-lookup"><span data-stu-id="6f8aa-132">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject, ExtendContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f8aa-133">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="6f8aa-133">-ContainerName</span></span>
<span data-ttu-id="6f8aa-134">Containername</span><span class="sxs-lookup"><span data-stu-id="6f8aa-134">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName, AccountObject, ExtendAccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f8aa-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f8aa-135">-DefaultProfile</span></span>
<span data-ttu-id="6f8aa-136">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f8aa-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f8aa-137">-Etag</span><span class="sxs-lookup"><span data-stu-id="6f8aa-137">-Etag</span></span>
<span data-ttu-id="6f8aa-138">E-Tag für Unveränderlichkeitsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="6f8aa-138">Immutability policy etag.</span></span> <span data-ttu-id="6f8aa-139">Wenn -ExtendPolicy nicht angegeben ist, ist Etag optional. sonst ist Etag erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6f8aa-139">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8aa-140">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="6f8aa-140">-ExtendPolicy</span></span>
<span data-ttu-id="6f8aa-141">Geben Sie ExtendPolicy an, um eine vorhandene ImmutabilityPolicy zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="6f8aa-141">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="6f8aa-142">Nachdem ImmutabilityPolicy gesperrt wurde, kann es nur noch erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="6f8aa-142">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8aa-143">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="6f8aa-143">-ImmutabilityPeriod</span></span>
<span data-ttu-id="6f8aa-144">Unveränderlichkeitszeitraum seit der Erstellung in Tagen.</span><span class="sxs-lookup"><span data-stu-id="6f8aa-144">Immutability period since creation in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8aa-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f8aa-145">-InputObject</span></span>
<span data-ttu-id="6f8aa-146">Containername</span><span class="sxs-lookup"><span data-stu-id="6f8aa-146">Container Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f8aa-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f8aa-147">-ResourceGroupName</span></span>
<span data-ttu-id="6f8aa-148">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="6f8aa-148">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f8aa-149">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f8aa-149">-StorageAccount</span></span>
<span data-ttu-id="6f8aa-150">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="6f8aa-150">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, ExtendAccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f8aa-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6f8aa-151">-StorageAccountName</span></span>
<span data-ttu-id="6f8aa-152">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="6f8aa-152">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f8aa-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6f8aa-153">-Confirm</span></span>
<span data-ttu-id="6f8aa-154">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6f8aa-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f8aa-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f8aa-155">-WhatIf</span></span>
<span data-ttu-id="6f8aa-156">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6f8aa-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f8aa-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f8aa-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f8aa-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f8aa-158">CommonParameters</span></span>
<span data-ttu-id="6f8aa-159">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f8aa-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f8aa-160">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f8aa-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f8aa-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6f8aa-161">INPUTS</span></span>

### <span data-ttu-id="6f8aa-162">System.String</span><span class="sxs-lookup"><span data-stu-id="6f8aa-162">System.String</span></span>

### <span data-ttu-id="6f8aa-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f8aa-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="6f8aa-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="6f8aa-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="6f8aa-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6f8aa-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="6f8aa-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6f8aa-166">OUTPUTS</span></span>

### <span data-ttu-id="6f8aa-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6f8aa-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="6f8aa-168">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6f8aa-168">NOTES</span></span>

## <span data-ttu-id="6f8aa-169">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6f8aa-169">RELATED LINKS</span></span>
