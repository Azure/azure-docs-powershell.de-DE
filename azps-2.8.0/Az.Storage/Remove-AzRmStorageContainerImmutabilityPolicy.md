---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: f0054a038745c2a15089f99c386c0ffb1bd6ccf9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826747"
---
# <span data-ttu-id="a3215-101">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a3215-101">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="a3215-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a3215-102">SYNOPSIS</span></span>
<span data-ttu-id="a3215-103">Entfernt ImmutabilityPolicy eines Speicher-BLOB-Containers mit einer freigegebenen Richtlinie</span><span class="sxs-lookup"><span data-stu-id="a3215-103">Removes ImmutabilityPolicy of a Storage blob container with an unlocked policy</span></span>

## <span data-ttu-id="a3215-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3215-104">SYNTAX</span></span>

### <span data-ttu-id="a3215-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="a3215-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3215-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="a3215-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3215-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="a3215-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3215-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="a3215-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3215-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3215-109">DESCRIPTION</span></span>
<span data-ttu-id="a3215-110">Das Cmdlet **Remove-AzRmStorageContainerImmutabilityPolicy** entfernt ImmutabilityPolicy eines Speicher-BLOB-Containers mit einer Unlocked-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="a3215-110">The **Remove-AzRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob container with an unlocked policy.</span></span>

## <span data-ttu-id="a3215-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3215-111">EXAMPLES</span></span>

### <span data-ttu-id="a3215-112">Beispiel 1: Entfernen von gesperrten ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="a3215-112">Example 1: Remove unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="a3215-113">Dieser Befehl entfernt gesperrte ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="a3215-113">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="a3215-114">Beispiel 2: Entfernen von gesperrten ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="a3215-114">Example 2: Remove unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="a3215-115">Dieser Befehl entfernt gesperrte ImmutabilityPolicy eines BLOB-Speichercontainers mit dem Speicherkonto Objekt.</span><span class="sxs-lookup"><span data-stu-id="a3215-115">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="a3215-116">Beispiel 3: Entfernen von gesperrten ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Container-Objekt</span><span class="sxs-lookup"><span data-stu-id="a3215-116">Example 3: Remove unlocked ImmutabilityPolicy of a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="a3215-117">Dieser Befehl entfernt gesperrte ImmutabilityPolicy eines Speicher-BLOB-Containers mit einem Speichercontainer Objekt.</span><span class="sxs-lookup"><span data-stu-id="a3215-117">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="a3215-118">Beispiel 4: Entfernen von gesperrten ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem ImmutabilityPolicy-Objekt</span><span class="sxs-lookup"><span data-stu-id="a3215-118">Example 4: Remove unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="a3215-119">Dieser Befehl entfernt gesperrte ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem ImmutabilityPolicy-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a3215-119">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="a3215-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3215-120">PARAMETERS</span></span>

### <span data-ttu-id="a3215-121">-Container</span><span class="sxs-lookup"><span data-stu-id="a3215-121">-Container</span></span>
<span data-ttu-id="a3215-122">Speichercontainer Objekt</span><span class="sxs-lookup"><span data-stu-id="a3215-122">Storage container object</span></span>

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

### <span data-ttu-id="a3215-123">-Containername</span><span class="sxs-lookup"><span data-stu-id="a3215-123">-ContainerName</span></span>
<span data-ttu-id="a3215-124">Container Name</span><span class="sxs-lookup"><span data-stu-id="a3215-124">Container Name</span></span>

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

### <span data-ttu-id="a3215-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3215-125">-DefaultProfile</span></span>
<span data-ttu-id="a3215-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a3215-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3215-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="a3215-127">-Etag</span></span>
<span data-ttu-id="a3215-128">Unveränderlichkeits Richtlinien-ETag.</span><span class="sxs-lookup"><span data-stu-id="a3215-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="a3215-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a3215-129">-InputObject</span></span>
<span data-ttu-id="a3215-130">Unlocked ImmutabilityPolicy-Objekt zum Entfernen</span><span class="sxs-lookup"><span data-stu-id="a3215-130">Unlocked ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="a3215-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3215-131">-ResourceGroupName</span></span>
<span data-ttu-id="a3215-132">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a3215-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="a3215-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a3215-133">-StorageAccount</span></span>
<span data-ttu-id="a3215-134">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="a3215-134">Storage account object</span></span>

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

### <span data-ttu-id="a3215-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a3215-135">-StorageAccountName</span></span>
<span data-ttu-id="a3215-136">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="a3215-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="a3215-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a3215-137">-Confirm</span></span>
<span data-ttu-id="a3215-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3215-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3215-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3215-139">-WhatIf</span></span>
<span data-ttu-id="a3215-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3215-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3215-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3215-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3215-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3215-142">CommonParameters</span></span>
<span data-ttu-id="a3215-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3215-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3215-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3215-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3215-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a3215-145">INPUTS</span></span>

### <span data-ttu-id="a3215-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a3215-146">System.String</span></span>

### <span data-ttu-id="a3215-147">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a3215-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="a3215-148">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="a3215-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="a3215-149">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a3215-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="a3215-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a3215-150">OUTPUTS</span></span>

### <span data-ttu-id="a3215-151">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a3215-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="a3215-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="a3215-152">NOTES</span></span>

## <span data-ttu-id="a3215-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a3215-153">RELATED LINKS</span></span>
