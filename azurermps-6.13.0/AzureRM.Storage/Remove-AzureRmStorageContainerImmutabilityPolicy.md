---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 74963ef36a33bed6145d315f5792aa776a36bc7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498158"
---
# <span data-ttu-id="4ada4-101">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="4ada4-101">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="4ada4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ada4-102">SYNOPSIS</span></span>
<span data-ttu-id="4ada4-103">Entfernt ImmutabilityPolicy eines Speicher-BLOB-Containers</span><span class="sxs-lookup"><span data-stu-id="4ada4-103">Removes ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ada4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ada4-104">SYNTAX</span></span>

### <span data-ttu-id="4ada4-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="4ada4-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ada4-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="4ada4-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ada4-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="4ada4-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ada4-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="4ada4-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ada4-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ada4-109">DESCRIPTION</span></span>
<span data-ttu-id="4ada4-110">Das Cmdlet **Remove-AzureRmStorageContainerImmutabilityPolicy** entfernt ImmutabilityPolicy eines Speicher-BLOB-Containers.</span><span class="sxs-lookup"><span data-stu-id="4ada4-110">The **Remove-AzureRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="4ada4-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ada4-111">EXAMPLES</span></span>

### <span data-ttu-id="4ada4-112">Beispiel 1: Entfernen von ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="4ada4-112">Example 1: Remove ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="4ada4-113">Dieser Befehl entfernt ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="4ada4-113">This command removes ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="4ada4-114">Beispiel 2: Entfernen von ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="4ada4-114">Example 2: Remove ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="4ada4-115">Dieser Befehl entfernt ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt.</span><span class="sxs-lookup"><span data-stu-id="4ada4-115">This command removes ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="4ada4-116">Beispiel 3: Entfernen von ImmutabilityPolicyof einem BLOB-Speichercontainer mit Containerobjekt</span><span class="sxs-lookup"><span data-stu-id="4ada4-116">Example 3: Remove ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="4ada4-117">Dieser Befehl entfernt ImmutabilityPolicy eines Speicher-BLOB-Containers mit einem Speichercontainer Objekt.</span><span class="sxs-lookup"><span data-stu-id="4ada4-117">This command removes ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="4ada4-118">Beispiel 4: Entfernen von ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem ImmutabilityPolicy-Objekt</span><span class="sxs-lookup"><span data-stu-id="4ada4-118">Example 4: Remove ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzureRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="4ada4-119">Dieser Befehl entfernt ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem ImmutabilityPolicy-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4ada4-119">This command removes ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="4ada4-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ada4-120">PARAMETERS</span></span>

### <span data-ttu-id="4ada4-121">-Container</span><span class="sxs-lookup"><span data-stu-id="4ada4-121">-Container</span></span>
<span data-ttu-id="4ada4-122">Speichercontainer Objekt</span><span class="sxs-lookup"><span data-stu-id="4ada4-122">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ada4-123">-Containername</span><span class="sxs-lookup"><span data-stu-id="4ada4-123">-ContainerName</span></span>
<span data-ttu-id="4ada4-124">Container Name</span><span class="sxs-lookup"><span data-stu-id="4ada4-124">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ada4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ada4-125">-DefaultProfile</span></span>
<span data-ttu-id="4ada4-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4ada4-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ada4-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="4ada4-127">-Etag</span></span>
<span data-ttu-id="4ada4-128">Unveränderlichkeits Richtlinien-ETag.</span><span class="sxs-lookup"><span data-stu-id="4ada4-128">Immutability policy etag.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ada4-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4ada4-129">-InputObject</span></span>
<span data-ttu-id="4ada4-130">Zu entfernendes ImmutabilityPolicy-Objekt</span><span class="sxs-lookup"><span data-stu-id="4ada4-130">ImmutabilityPolicy Object to Remove</span></span>

```yaml
Type: PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ada4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ada4-131">-ResourceGroupName</span></span>
<span data-ttu-id="4ada4-132">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4ada4-132">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ada4-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ada4-133">-StorageAccount</span></span>
<span data-ttu-id="4ada4-134">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="4ada4-134">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ada4-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4ada4-135">-StorageAccountName</span></span>
<span data-ttu-id="4ada4-136">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="4ada4-136">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ada4-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4ada4-137">-Confirm</span></span>
<span data-ttu-id="4ada4-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4ada4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ada4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ada4-139">-WhatIf</span></span>
<span data-ttu-id="4ada4-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4ada4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ada4-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ada4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ada4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ada4-142">CommonParameters</span></span>
<span data-ttu-id="4ada4-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ada4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ada4-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ada4-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ada4-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ada4-145">INPUTS</span></span>

### <span data-ttu-id="4ada4-146">System. String</span><span class="sxs-lookup"><span data-stu-id="4ada4-146">System.String</span></span>
<span data-ttu-id="4ada4-147">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="4ada4-147">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="4ada4-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ada4-148">OUTPUTS</span></span>

### <span data-ttu-id="4ada4-149">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="4ada4-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="4ada4-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ada4-150">NOTES</span></span>

## <span data-ttu-id="4ada4-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ada4-151">RELATED LINKS</span></span>

