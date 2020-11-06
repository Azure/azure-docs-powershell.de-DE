---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/lock-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Lock-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Lock-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 726dc9043c1082f97e32da46305cf81192e1806c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93475925"
---
# <span data-ttu-id="95bc2-101">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="95bc2-101">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="95bc2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="95bc2-102">SYNOPSIS</span></span>
<span data-ttu-id="95bc2-103">Sperrt ImmutabilityPolicy eines Speicher-BLOB-Containers</span><span class="sxs-lookup"><span data-stu-id="95bc2-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95bc2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="95bc2-104">SYNTAX</span></span>

### <span data-ttu-id="95bc2-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="95bc2-105">AccountName (Default)</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95bc2-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="95bc2-106">AccountObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95bc2-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="95bc2-107">ContainerObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95bc2-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="95bc2-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95bc2-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95bc2-109">DESCRIPTION</span></span>
<span data-ttu-id="95bc2-110">Das **Lock-AzureRmStorageContainerImmutabilityPolicy-** Cmdlet sperrt ImmutabilityPolicy eines Speicher-BLOB-Containers.</span><span class="sxs-lookup"><span data-stu-id="95bc2-110">The **Lock-AzureRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="95bc2-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="95bc2-111">EXAMPLES</span></span>

### <span data-ttu-id="95bc2-112">Beispiel 1: Sperren des ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="95bc2-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="95bc2-113">Dieser Befehl sperrt ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="95bc2-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="95bc2-114">Beispiel 2: Sperren von ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="95bc2-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="95bc2-115">Dieser Befehl sperrt ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt.</span><span class="sxs-lookup"><span data-stu-id="95bc2-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="95bc2-116">Beispiel 3: Sperren des ImmutabilityPolicyof eines Speicher-BLOB-Containers mit Container-Objekt</span><span class="sxs-lookup"><span data-stu-id="95bc2-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="95bc2-117">Dieser Befehl sperrt ImmutabilityPolicy eines Speicher-BLOB-Containers mit einem Speichercontainer Objekt.</span><span class="sxs-lookup"><span data-stu-id="95bc2-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="95bc2-118">Beispiel 4: Sperren von ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem ImmutabilityPolicy-Objekt</span><span class="sxs-lookup"><span data-stu-id="95bc2-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzureRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="95bc2-119">Dieser Befehl sperrt ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem ImmutabilityPolicy-Objekt.</span><span class="sxs-lookup"><span data-stu-id="95bc2-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="95bc2-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="95bc2-120">PARAMETERS</span></span>

### <span data-ttu-id="95bc2-121">-Container</span><span class="sxs-lookup"><span data-stu-id="95bc2-121">-Container</span></span>
<span data-ttu-id="95bc2-122">Speichercontainer Objekt</span><span class="sxs-lookup"><span data-stu-id="95bc2-122">Storage container object</span></span>

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

### <span data-ttu-id="95bc2-123">-Containername</span><span class="sxs-lookup"><span data-stu-id="95bc2-123">-ContainerName</span></span>
<span data-ttu-id="95bc2-124">Container Name</span><span class="sxs-lookup"><span data-stu-id="95bc2-124">Container Name</span></span>

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

### <span data-ttu-id="95bc2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95bc2-125">-DefaultProfile</span></span>
<span data-ttu-id="95bc2-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="95bc2-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95bc2-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="95bc2-127">-Etag</span></span>
<span data-ttu-id="95bc2-128">Unveränderlichkeits Richtlinien-ETag.</span><span class="sxs-lookup"><span data-stu-id="95bc2-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="95bc2-129">-Force</span><span class="sxs-lookup"><span data-stu-id="95bc2-129">-Force</span></span>
<span data-ttu-id="95bc2-130">Erzwingen des Entfernens des ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="95bc2-130">Force to remove the ImmutabilityPolicy.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95bc2-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="95bc2-131">-InputObject</span></span>
<span data-ttu-id="95bc2-132">Zu entfernendes ImmutabilityPolicy-Objekt</span><span class="sxs-lookup"><span data-stu-id="95bc2-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="95bc2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95bc2-133">-ResourceGroupName</span></span>
<span data-ttu-id="95bc2-134">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="95bc2-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="95bc2-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="95bc2-135">-StorageAccount</span></span>
<span data-ttu-id="95bc2-136">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="95bc2-136">Storage account object</span></span>

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

### <span data-ttu-id="95bc2-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="95bc2-137">-StorageAccountName</span></span>
<span data-ttu-id="95bc2-138">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="95bc2-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="95bc2-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="95bc2-139">-Confirm</span></span>
<span data-ttu-id="95bc2-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="95bc2-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95bc2-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95bc2-141">-WhatIf</span></span>
<span data-ttu-id="95bc2-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="95bc2-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95bc2-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95bc2-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95bc2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95bc2-144">CommonParameters</span></span>
<span data-ttu-id="95bc2-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95bc2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95bc2-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95bc2-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95bc2-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="95bc2-147">INPUTS</span></span>

### <span data-ttu-id="95bc2-148">System. String</span><span class="sxs-lookup"><span data-stu-id="95bc2-148">System.String</span></span>
<span data-ttu-id="95bc2-149">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="95bc2-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="95bc2-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="95bc2-150">OUTPUTS</span></span>

### <span data-ttu-id="95bc2-151">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="95bc2-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="95bc2-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="95bc2-152">NOTES</span></span>

## <span data-ttu-id="95bc2-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="95bc2-153">RELATED LINKS</span></span>

