---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: c216765657cc87c958cc20dd0f2014f0e1c16970
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658757"
---
# <span data-ttu-id="53031-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="53031-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="53031-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="53031-102">SYNOPSIS</span></span>
<span data-ttu-id="53031-103">Erstellt oder aktualisiert ImmutabilityPolicy eines Speicher-BLOB-Containers</span><span class="sxs-lookup"><span data-stu-id="53031-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="53031-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="53031-104">SYNTAX</span></span>

### <span data-ttu-id="53031-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="53031-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53031-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="53031-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53031-107">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="53031-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53031-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="53031-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53031-109">Containerobject</span><span class="sxs-lookup"><span data-stu-id="53031-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53031-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="53031-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53031-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="53031-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53031-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="53031-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53031-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53031-113">DESCRIPTION</span></span>
<span data-ttu-id="53031-114">Das Cmdlet " **Satz-AzRmStorageContainerImmutabilityPolicy** " erstellt oder aktualisiert ImmutabilityPolicy eines Speicher-BLOB-Containers</span><span class="sxs-lookup"><span data-stu-id="53031-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="53031-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53031-115">EXAMPLES</span></span>

### <span data-ttu-id="53031-116">Beispiel 1: Erstellen oder Aktualisieren von ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="53031-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="53031-117">Dieser Befehl erstellt oder aktualisiert ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="53031-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="53031-118">Beispiel 2: Erweitern des ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="53031-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="53031-119">Dieser Befehl erweitert ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt.</span><span class="sxs-lookup"><span data-stu-id="53031-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="53031-120">Extend ImmutabilityPolicy kann nur ausgeführt werden, nachdem ImmutabilityPolicy gesperrt wurde.</span><span class="sxs-lookup"><span data-stu-id="53031-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="53031-121">Beispiel 3: Aktualisieren des ImmutabilityPolicyof eines Speicher-BLOB-Containers</span><span class="sxs-lookup"><span data-stu-id="53031-121">Example 3: Update ImmutabilityPolicyof a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
```

<span data-ttu-id="53031-122">Dieser Befehl aktualisiert ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Speichercontainer Objekt 2 Mal, zunächst ImmutabilityPeriod 12 Tage ohne ETag, dann auf ImmutabilityPeriod 9 Tage mit ETag.</span><span class="sxs-lookup"><span data-stu-id="53031-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 2 times, first to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag.</span></span>

### <span data-ttu-id="53031-123">Beispiel 4: Erweitern des ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem ImmutabilityPolicy-Objekt</span><span class="sxs-lookup"><span data-stu-id="53031-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="53031-124">Dieser Befehl erweitert ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem ImmutabilityPolicy-Objekt.</span><span class="sxs-lookup"><span data-stu-id="53031-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="53031-125">Extend ImmutabilityPolicy kann nur ausgeführt werden, nachdem ImmutabilityPolicy gesperrt wurde.</span><span class="sxs-lookup"><span data-stu-id="53031-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="53031-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="53031-126">PARAMETERS</span></span>

### <span data-ttu-id="53031-127">-Container</span><span class="sxs-lookup"><span data-stu-id="53031-127">-Container</span></span>
<span data-ttu-id="53031-128">Speichercontainer Objekt</span><span class="sxs-lookup"><span data-stu-id="53031-128">Storage container object</span></span>

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

### <span data-ttu-id="53031-129">-Containername</span><span class="sxs-lookup"><span data-stu-id="53031-129">-ContainerName</span></span>
<span data-ttu-id="53031-130">Container Name</span><span class="sxs-lookup"><span data-stu-id="53031-130">Container Name</span></span>

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

### <span data-ttu-id="53031-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53031-131">-DefaultProfile</span></span>
<span data-ttu-id="53031-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="53031-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53031-133">-ETag</span><span class="sxs-lookup"><span data-stu-id="53031-133">-Etag</span></span>
<span data-ttu-id="53031-134">Unveränderlichkeits Richtlinien-ETag.</span><span class="sxs-lookup"><span data-stu-id="53031-134">Immutability policy etag.</span></span> <span data-ttu-id="53031-135">Wenn-ExtendPolicy nicht angegeben ist, ist ETag optional; Else ETag ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="53031-135">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

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

### <span data-ttu-id="53031-136">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="53031-136">-ExtendPolicy</span></span>
<span data-ttu-id="53031-137">Geben Sie ExtendPolicy an, um eine vorhandene ImmutabilityPolicy zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="53031-137">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="53031-138">Nachdem ImmutabilityPolicy gesperrt wurde, kann es nur verlängert werden.</span><span class="sxs-lookup"><span data-stu-id="53031-138">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

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

### <span data-ttu-id="53031-139">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="53031-139">-ImmutabilityPeriod</span></span>
<span data-ttu-id="53031-140">Unveränderlichkeits Zeitraum seit der Erstellung in Tagen.</span><span class="sxs-lookup"><span data-stu-id="53031-140">Immutability period since creation in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53031-141">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="53031-141">-InputObject</span></span>
<span data-ttu-id="53031-142">Container Name</span><span class="sxs-lookup"><span data-stu-id="53031-142">Container Name</span></span>

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

### <span data-ttu-id="53031-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53031-143">-ResourceGroupName</span></span>
<span data-ttu-id="53031-144">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="53031-144">Resource Group Name.</span></span>

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

### <span data-ttu-id="53031-145">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="53031-145">-StorageAccount</span></span>
<span data-ttu-id="53031-146">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="53031-146">Storage account object</span></span>

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

### <span data-ttu-id="53031-147">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="53031-147">-StorageAccountName</span></span>
<span data-ttu-id="53031-148">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="53031-148">Storage Account Name.</span></span>

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

### <span data-ttu-id="53031-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="53031-149">-Confirm</span></span>
<span data-ttu-id="53031-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="53031-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53031-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53031-151">-WhatIf</span></span>
<span data-ttu-id="53031-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="53031-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53031-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="53031-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53031-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53031-154">CommonParameters</span></span>
<span data-ttu-id="53031-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53031-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53031-156">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53031-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53031-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="53031-157">INPUTS</span></span>

### <span data-ttu-id="53031-158">System. String</span><span class="sxs-lookup"><span data-stu-id="53031-158">System.String</span></span>

### <span data-ttu-id="53031-159">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53031-159">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="53031-160">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="53031-160">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="53031-161">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="53031-161">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="53031-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="53031-162">OUTPUTS</span></span>

### <span data-ttu-id="53031-163">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="53031-163">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="53031-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="53031-164">NOTES</span></span>

## <span data-ttu-id="53031-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="53031-165">RELATED LINKS</span></span>
