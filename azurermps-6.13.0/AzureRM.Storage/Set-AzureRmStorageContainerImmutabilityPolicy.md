---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/set-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 7717aaa76efba736015a1cf762c95af440b28218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498149"
---
# <span data-ttu-id="af42e-101">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="af42e-101">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="af42e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="af42e-102">SYNOPSIS</span></span>
<span data-ttu-id="af42e-103">Erstellt oder aktualisiert ImmutabilityPolicy eines Speicher-BLOB-Containers</span><span class="sxs-lookup"><span data-stu-id="af42e-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af42e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="af42e-104">SYNTAX</span></span>

### <span data-ttu-id="af42e-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="af42e-105">AccountName (Default)</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> -ImmutabilityPeriod <Int32> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af42e-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="af42e-106">ExtendAccountName</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af42e-107">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="af42e-107">AccountObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af42e-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="af42e-108">ExtendAccountObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af42e-109">Containerobject</span><span class="sxs-lookup"><span data-stu-id="af42e-109">ContainerObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af42e-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="af42e-110">ExtendContainerObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af42e-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="af42e-111">ImmutabilityPolicyObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af42e-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="af42e-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af42e-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="af42e-113">DESCRIPTION</span></span>
<span data-ttu-id="af42e-114">Das Cmdlet " **Satz-AzureRmStorageContainerImmutabilityPolicy** " erstellt oder aktualisiert ImmutabilityPolicy eines Speicher-BLOB-Containers</span><span class="sxs-lookup"><span data-stu-id="af42e-114">The **Set-AzureRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="af42e-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="af42e-115">EXAMPLES</span></span>

### <span data-ttu-id="af42e-116">Beispiel 1: Erstellen oder Aktualisieren von ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="af42e-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10 
```

<span data-ttu-id="af42e-117">Dieser Befehl erstellt oder aktualisiert ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="af42e-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="af42e-118">Beispiel 2: Erweitern des ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="af42e-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="af42e-119">Dieser Befehl erweitert ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt.</span><span class="sxs-lookup"><span data-stu-id="af42e-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="af42e-120">Extend ImmutabilityPolicy kann nur ausgeführt werden, nachdem ImmutabilityPolicy gesperrt wurde.</span><span class="sxs-lookup"><span data-stu-id="af42e-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="af42e-121">Beispiel 3: Aktualisieren des ImmutabilityPolicyof eines Speicher-BLOB-Containers</span><span class="sxs-lookup"><span data-stu-id="af42e-121">Example 3: Update ImmutabilityPolicyof a Storage blob container</span></span> 
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
```

<span data-ttu-id="af42e-122">Dieser Befehl aktualisiert ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Speichercontainer Objekt 2 Mal, zunächst ImmutabilityPeriod 12 Tage ohne ETag, dann auf ImmutabilityPeriod 9 Tage mit ETag.</span><span class="sxs-lookup"><span data-stu-id="af42e-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 2 times, first to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag.</span></span>

### <span data-ttu-id="af42e-123">Beispiel 4: Erweitern des ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem ImmutabilityPolicy-Objekt</span><span class="sxs-lookup"><span data-stu-id="af42e-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzureRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="af42e-124">Dieser Befehl erweitert ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem ImmutabilityPolicy-Objekt.</span><span class="sxs-lookup"><span data-stu-id="af42e-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="af42e-125">Extend ImmutabilityPolicy kann nur ausgeführt werden, nachdem ImmutabilityPolicy gesperrt wurde.</span><span class="sxs-lookup"><span data-stu-id="af42e-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="af42e-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="af42e-126">PARAMETERS</span></span>

### <span data-ttu-id="af42e-127">-Container</span><span class="sxs-lookup"><span data-stu-id="af42e-127">-Container</span></span>
<span data-ttu-id="af42e-128">Speichercontainer Objekt</span><span class="sxs-lookup"><span data-stu-id="af42e-128">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject, ExtendContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af42e-129">-Containername</span><span class="sxs-lookup"><span data-stu-id="af42e-129">-ContainerName</span></span>
<span data-ttu-id="af42e-130">Container Name</span><span class="sxs-lookup"><span data-stu-id="af42e-130">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName, AccountObject, ExtendAccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af42e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af42e-131">-DefaultProfile</span></span>
<span data-ttu-id="af42e-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="af42e-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af42e-133">-ETag</span><span class="sxs-lookup"><span data-stu-id="af42e-133">-Etag</span></span>
<span data-ttu-id="af42e-134">Unveränderlichkeits Richtlinien-ETag.</span><span class="sxs-lookup"><span data-stu-id="af42e-134">Immutability policy etag.</span></span> <span data-ttu-id="af42e-135">Wenn-ExtendPolicy nicht angegeben ist, ist ETag optional; Else ETag ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="af42e-135">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af42e-136">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="af42e-136">-ExtendPolicy</span></span>
<span data-ttu-id="af42e-137">Geben Sie ExtendPolicy an, um eine vorhandene ImmutabilityPolicy zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="af42e-137">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="af42e-138">Nachdem ImmutabilityPolicy gesperrt wurde, kann es nur verlängert werden.</span><span class="sxs-lookup"><span data-stu-id="af42e-138">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

```yaml
Type: SwitchParameter
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af42e-139">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="af42e-139">-ImmutabilityPeriod</span></span>
<span data-ttu-id="af42e-140">Unveränderlichkeits Zeitraum seit der Erstellung in Tagen.</span><span class="sxs-lookup"><span data-stu-id="af42e-140">Immutability period since creation in days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af42e-141">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="af42e-141">-InputObject</span></span>
<span data-ttu-id="af42e-142">Container Name</span><span class="sxs-lookup"><span data-stu-id="af42e-142">Container Name</span></span>

```yaml
Type: PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af42e-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af42e-143">-ResourceGroupName</span></span>
<span data-ttu-id="af42e-144">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="af42e-144">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af42e-145">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="af42e-145">-StorageAccount</span></span>
<span data-ttu-id="af42e-146">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="af42e-146">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject, ExtendAccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af42e-147">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="af42e-147">-StorageAccountName</span></span>
<span data-ttu-id="af42e-148">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="af42e-148">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af42e-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="af42e-149">-Confirm</span></span>
<span data-ttu-id="af42e-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="af42e-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af42e-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af42e-151">-WhatIf</span></span>
<span data-ttu-id="af42e-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="af42e-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af42e-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="af42e-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af42e-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af42e-154">CommonParameters</span></span>
<span data-ttu-id="af42e-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af42e-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af42e-156">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af42e-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af42e-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="af42e-157">INPUTS</span></span>

### <span data-ttu-id="af42e-158">System. String</span><span class="sxs-lookup"><span data-stu-id="af42e-158">System.String</span></span>
<span data-ttu-id="af42e-159">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="af42e-159">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="af42e-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="af42e-160">OUTPUTS</span></span>

### <span data-ttu-id="af42e-161">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="af42e-161">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="af42e-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="af42e-162">NOTES</span></span>

## <span data-ttu-id="af42e-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="af42e-163">RELATED LINKS</span></span>

