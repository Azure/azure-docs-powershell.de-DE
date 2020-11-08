---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 9631855803b4ad16312c907c1d1c747b3aee6fdf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173995"
---
# <span data-ttu-id="1c850-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1c850-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="1c850-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1c850-102">SYNOPSIS</span></span>
<span data-ttu-id="1c850-103">Erstellt oder aktualisiert ImmutabilityPolicy eines Speicher-BLOB-Containers</span><span class="sxs-lookup"><span data-stu-id="1c850-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="1c850-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c850-104">SYNTAX</span></span>

### <span data-ttu-id="1c850-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="1c850-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c850-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="1c850-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c850-107">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="1c850-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c850-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="1c850-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c850-109">Containerobject</span><span class="sxs-lookup"><span data-stu-id="1c850-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c850-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="1c850-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c850-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="1c850-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c850-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="1c850-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c850-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c850-113">DESCRIPTION</span></span>
<span data-ttu-id="1c850-114">Das Cmdlet " **Satz-AzRmStorageContainerImmutabilityPolicy** " erstellt oder aktualisiert ImmutabilityPolicy eines Speicher-BLOB-Containers</span><span class="sxs-lookup"><span data-stu-id="1c850-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="1c850-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c850-115">EXAMPLES</span></span>

### <span data-ttu-id="1c850-116">Beispiel 1: Erstellen oder Aktualisieren von ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="1c850-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="1c850-117">Dieser Befehl erstellt oder aktualisiert ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="1c850-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="1c850-118">Beispiel 2: Erweitern des ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="1c850-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="1c850-119">Dieser Befehl erweitert ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt.</span><span class="sxs-lookup"><span data-stu-id="1c850-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="1c850-120">Extend ImmutabilityPolicy kann nur ausgeführt werden, nachdem ImmutabilityPolicy gesperrt wurde.</span><span class="sxs-lookup"><span data-stu-id="1c850-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="1c850-121">Beispiel 3: Aktualisieren von ImmutabilityPolicy eines Speicher-BLOB-Containers</span><span class="sxs-lookup"><span data-stu-id="1c850-121">Example 3: Update ImmutabilityPolicy of a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -AllowProtectedAppendWrite $true
```

<span data-ttu-id="1c850-122">Dieser Befehl aktualisiert ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Speichercontainer Objekt dreimal: zuerst bis ImmutabilityPeriod 12 Tage ohne ETag, dann auf ImmutabilityPeriod 9 Tage mit ETag, schließlich aktiviert AllowProtectedAppendWrite.</span><span class="sxs-lookup"><span data-stu-id="1c850-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 3 times: First to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag, finally enabled AllowProtectedAppendWrite.</span></span>

### <span data-ttu-id="1c850-123">Beispiel 4: Erweitern des ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem ImmutabilityPolicy-Objekt</span><span class="sxs-lookup"><span data-stu-id="1c850-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="1c850-124">Dieser Befehl erweitert ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem ImmutabilityPolicy-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1c850-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="1c850-125">Extend ImmutabilityPolicy kann nur ausgeführt werden, nachdem ImmutabilityPolicy gesperrt wurde.</span><span class="sxs-lookup"><span data-stu-id="1c850-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="1c850-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c850-126">PARAMETERS</span></span>

### <span data-ttu-id="1c850-127">-AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="1c850-127">-AllowProtectedAppendWrite</span></span>
<span data-ttu-id="1c850-128">Diese Eigenschaft kann nur für freigegebene zeitbasierte Aufbewahrungsrichtlinien geändert werden.</span><span class="sxs-lookup"><span data-stu-id="1c850-128">This property can only be changed for unlocked time-based retention policies.</span></span> <span data-ttu-id="1c850-129">Wenn diese Eigenschaft aktiviert ist, können neue Blöcke in ein Append-BLOB geschrieben werden, wobei der Schutz und die Compliance unveränderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1c850-129">With this property enabled, new blocks can be written to an append blob while maintaining immutability protection and compliance.</span></span> <span data-ttu-id="1c850-130">Es können nur neue Blöcke hinzugefügt und vorhandene Blöcke nicht geändert oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="1c850-130">Only new blocks can be added and any existing blocks cannot be modified or deleted.</span></span>

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

### <span data-ttu-id="1c850-131">-Container</span><span class="sxs-lookup"><span data-stu-id="1c850-131">-Container</span></span>
<span data-ttu-id="1c850-132">Speichercontainer Objekt</span><span class="sxs-lookup"><span data-stu-id="1c850-132">Storage container object</span></span>

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

### <span data-ttu-id="1c850-133">-Containername</span><span class="sxs-lookup"><span data-stu-id="1c850-133">-ContainerName</span></span>
<span data-ttu-id="1c850-134">Container Name</span><span class="sxs-lookup"><span data-stu-id="1c850-134">Container Name</span></span>

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

### <span data-ttu-id="1c850-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c850-135">-DefaultProfile</span></span>
<span data-ttu-id="1c850-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1c850-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c850-137">-ETag</span><span class="sxs-lookup"><span data-stu-id="1c850-137">-Etag</span></span>
<span data-ttu-id="1c850-138">Unveränderlichkeits Richtlinien-ETag.</span><span class="sxs-lookup"><span data-stu-id="1c850-138">Immutability policy etag.</span></span> <span data-ttu-id="1c850-139">Wenn-ExtendPolicy nicht angegeben ist, ist ETag optional; Else ETag ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1c850-139">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

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

### <span data-ttu-id="1c850-140">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="1c850-140">-ExtendPolicy</span></span>
<span data-ttu-id="1c850-141">Geben Sie ExtendPolicy an, um eine vorhandene ImmutabilityPolicy zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="1c850-141">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="1c850-142">Nachdem ImmutabilityPolicy gesperrt wurde, kann es nur verlängert werden.</span><span class="sxs-lookup"><span data-stu-id="1c850-142">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

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

### <span data-ttu-id="1c850-143">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="1c850-143">-ImmutabilityPeriod</span></span>
<span data-ttu-id="1c850-144">Unveränderlichkeits Zeitraum seit der Erstellung in Tagen.</span><span class="sxs-lookup"><span data-stu-id="1c850-144">Immutability period since creation in days.</span></span>

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

### <span data-ttu-id="1c850-145">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1c850-145">-InputObject</span></span>
<span data-ttu-id="1c850-146">Container Name</span><span class="sxs-lookup"><span data-stu-id="1c850-146">Container Name</span></span>

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

### <span data-ttu-id="1c850-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c850-147">-ResourceGroupName</span></span>
<span data-ttu-id="1c850-148">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1c850-148">Resource Group Name.</span></span>

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

### <span data-ttu-id="1c850-149">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="1c850-149">-StorageAccount</span></span>
<span data-ttu-id="1c850-150">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="1c850-150">Storage account object</span></span>

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

### <span data-ttu-id="1c850-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1c850-151">-StorageAccountName</span></span>
<span data-ttu-id="1c850-152">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="1c850-152">Storage Account Name.</span></span>

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

### <span data-ttu-id="1c850-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1c850-153">-Confirm</span></span>
<span data-ttu-id="1c850-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c850-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c850-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c850-155">-WhatIf</span></span>
<span data-ttu-id="1c850-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c850-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c850-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c850-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c850-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c850-158">CommonParameters</span></span>
<span data-ttu-id="1c850-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c850-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c850-160">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c850-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c850-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c850-161">INPUTS</span></span>

### <span data-ttu-id="1c850-162">System. String</span><span class="sxs-lookup"><span data-stu-id="1c850-162">System.String</span></span>

### <span data-ttu-id="1c850-163">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1c850-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="1c850-164">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="1c850-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="1c850-165">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1c850-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="1c850-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1c850-166">OUTPUTS</span></span>

### <span data-ttu-id="1c850-167">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1c850-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="1c850-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="1c850-168">NOTES</span></span>

## <span data-ttu-id="1c850-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1c850-169">RELATED LINKS</span></span>
