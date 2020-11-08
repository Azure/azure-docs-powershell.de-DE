---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/lock-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 0cb3a4e65d8e464dda85e18e12dc106620e3eee8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176823"
---
# <span data-ttu-id="0989b-101">Lock-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0989b-101">Lock-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="0989b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0989b-102">SYNOPSIS</span></span>
<span data-ttu-id="0989b-103">Sperrt ImmutabilityPolicy eines Speicher-BLOB-Containers</span><span class="sxs-lookup"><span data-stu-id="0989b-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="0989b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0989b-104">SYNTAX</span></span>

### <span data-ttu-id="0989b-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="0989b-105">AccountName (Default)</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0989b-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="0989b-106">AccountObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0989b-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="0989b-107">ContainerObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0989b-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="0989b-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0989b-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0989b-109">DESCRIPTION</span></span>
<span data-ttu-id="0989b-110">Das **Lock-AzRmStorageContainerImmutabilityPolicy-** Cmdlet sperrt ImmutabilityPolicy eines Speicher-BLOB-Containers.</span><span class="sxs-lookup"><span data-stu-id="0989b-110">The **Lock-AzRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="0989b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0989b-111">EXAMPLES</span></span>

### <span data-ttu-id="0989b-112">Beispiel 1: Sperren des ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="0989b-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="0989b-113">Dieser Befehl sperrt ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="0989b-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="0989b-114">Beispiel 2: Sperren von ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="0989b-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="0989b-115">Dieser Befehl sperrt ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt.</span><span class="sxs-lookup"><span data-stu-id="0989b-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="0989b-116">Beispiel 3: Sperren des ImmutabilityPolicyof eines Speicher-BLOB-Containers mit Container-Objekt</span><span class="sxs-lookup"><span data-stu-id="0989b-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="0989b-117">Dieser Befehl sperrt ImmutabilityPolicy eines Speicher-BLOB-Containers mit einem Speichercontainer Objekt.</span><span class="sxs-lookup"><span data-stu-id="0989b-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="0989b-118">Beispiel 4: Sperren von ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem ImmutabilityPolicy-Objekt</span><span class="sxs-lookup"><span data-stu-id="0989b-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="0989b-119">Dieser Befehl sperrt ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem ImmutabilityPolicy-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0989b-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="0989b-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="0989b-120">PARAMETERS</span></span>

### <span data-ttu-id="0989b-121">-Container</span><span class="sxs-lookup"><span data-stu-id="0989b-121">-Container</span></span>
<span data-ttu-id="0989b-122">Speichercontainer Objekt</span><span class="sxs-lookup"><span data-stu-id="0989b-122">Storage container object</span></span>

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

### <span data-ttu-id="0989b-123">-Containername</span><span class="sxs-lookup"><span data-stu-id="0989b-123">-ContainerName</span></span>
<span data-ttu-id="0989b-124">Container Name</span><span class="sxs-lookup"><span data-stu-id="0989b-124">Container Name</span></span>

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

### <span data-ttu-id="0989b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0989b-125">-DefaultProfile</span></span>
<span data-ttu-id="0989b-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0989b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0989b-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="0989b-127">-Etag</span></span>
<span data-ttu-id="0989b-128">Unveränderlichkeits Richtlinien-ETag.</span><span class="sxs-lookup"><span data-stu-id="0989b-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="0989b-129">-Force</span><span class="sxs-lookup"><span data-stu-id="0989b-129">-Force</span></span>
<span data-ttu-id="0989b-130">Erzwingen des Entfernens des ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0989b-130">Force to remove the ImmutabilityPolicy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0989b-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0989b-131">-InputObject</span></span>
<span data-ttu-id="0989b-132">Zu entfernendes ImmutabilityPolicy-Objekt</span><span class="sxs-lookup"><span data-stu-id="0989b-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="0989b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0989b-133">-ResourceGroupName</span></span>
<span data-ttu-id="0989b-134">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0989b-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="0989b-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="0989b-135">-StorageAccount</span></span>
<span data-ttu-id="0989b-136">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="0989b-136">Storage account object</span></span>

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

### <span data-ttu-id="0989b-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0989b-137">-StorageAccountName</span></span>
<span data-ttu-id="0989b-138">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="0989b-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="0989b-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0989b-139">-Confirm</span></span>
<span data-ttu-id="0989b-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0989b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0989b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0989b-141">-WhatIf</span></span>
<span data-ttu-id="0989b-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0989b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0989b-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0989b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0989b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0989b-144">CommonParameters</span></span>
<span data-ttu-id="0989b-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0989b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0989b-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0989b-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0989b-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0989b-147">INPUTS</span></span>

### <span data-ttu-id="0989b-148">System. String</span><span class="sxs-lookup"><span data-stu-id="0989b-148">System.String</span></span>

### <span data-ttu-id="0989b-149">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0989b-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="0989b-150">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="0989b-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="0989b-151">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0989b-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="0989b-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0989b-152">OUTPUTS</span></span>

### <span data-ttu-id="0989b-153">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0989b-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="0989b-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="0989b-154">NOTES</span></span>

## <span data-ttu-id="0989b-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0989b-155">RELATED LINKS</span></span>
