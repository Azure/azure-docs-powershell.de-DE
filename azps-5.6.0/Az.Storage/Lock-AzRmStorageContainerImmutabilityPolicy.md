---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/lock-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 44d0f6b9717e51aec508da76a9ef9b776891d8c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940739"
---
# <span data-ttu-id="c5aec-101">Lock-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c5aec-101">Lock-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="c5aec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5aec-102">SYNOPSIS</span></span>
<span data-ttu-id="c5aec-103">Sperrt ImmutabilityPolicy eines Speicherblobcontainers</span><span class="sxs-lookup"><span data-stu-id="c5aec-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="c5aec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5aec-104">SYNTAX</span></span>

### <span data-ttu-id="c5aec-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c5aec-105">AccountName (Default)</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5aec-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="c5aec-106">AccountObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5aec-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="c5aec-107">ContainerObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5aec-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="c5aec-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5aec-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5aec-109">DESCRIPTION</span></span>
<span data-ttu-id="c5aec-110">Das **Lock-AzRmStorageContainerImmutabilityPolicy-Cmdlet** sperrt ImmutabilityPolicy eines Speicherblobscontainers.</span><span class="sxs-lookup"><span data-stu-id="c5aec-110">The **Lock-AzRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="c5aec-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c5aec-111">EXAMPLES</span></span>

### <span data-ttu-id="c5aec-112">Beispiel 1: Sperren von ImmutbarkeitPolicy eines Speicherblobcontainers mit Dem Namen des Speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="c5aec-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="c5aec-113">Mit diesem Befehl wird ImmutabilityPolicy eines Speicherblobcontainers mit dem Namen des Speicherkontos und dem Containernamen gesperrt.</span><span class="sxs-lookup"><span data-stu-id="c5aec-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="c5aec-114">Beispiel 2: Sperren der ImmutbarkeitPolicy eines Speicherblobcontainers mit Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="c5aec-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="c5aec-115">Mit diesem Befehl wird ImmutabilityPolicy eines Speicherblobcontainers mit Speicherkontoobjekt gesperrt.</span><span class="sxs-lookup"><span data-stu-id="c5aec-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="c5aec-116">Beispiel 3: Sperren von ImmutabilityPolicyof eines Speicherblobcontainers mit Containerobjekt</span><span class="sxs-lookup"><span data-stu-id="c5aec-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="c5aec-117">Dieser Befehl sperrt ImmutabilityPolicy eines Speicher-Blob-Containers mit Speichercontainerobjekt.</span><span class="sxs-lookup"><span data-stu-id="c5aec-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="c5aec-118">Beispiel 4: Sperren von ImmutabilityPolicy eines Speicherblobcontainers mit ImmutabilityPolicy-Objekt</span><span class="sxs-lookup"><span data-stu-id="c5aec-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="c5aec-119">Mit diesem Befehl wird ImmutabilityPolicy eines Speicherblobcontainers mit dem ImmutabilityPolicy-Objekt gesperrt.</span><span class="sxs-lookup"><span data-stu-id="c5aec-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="c5aec-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c5aec-120">PARAMETERS</span></span>

### <span data-ttu-id="c5aec-121">-Container</span><span class="sxs-lookup"><span data-stu-id="c5aec-121">-Container</span></span>
<span data-ttu-id="c5aec-122">Speichercontainerobjekt</span><span class="sxs-lookup"><span data-stu-id="c5aec-122">Storage container object</span></span>

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

### <span data-ttu-id="c5aec-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="c5aec-123">-ContainerName</span></span>
<span data-ttu-id="c5aec-124">Containername</span><span class="sxs-lookup"><span data-stu-id="c5aec-124">Container Name</span></span>

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

### <span data-ttu-id="c5aec-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5aec-125">-DefaultProfile</span></span>
<span data-ttu-id="c5aec-126">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5aec-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5aec-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="c5aec-127">-Etag</span></span>
<span data-ttu-id="c5aec-128">E-Tag für Unveränderlichkeitsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="c5aec-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="c5aec-129">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="c5aec-129">-Force</span></span>
<span data-ttu-id="c5aec-130">Erzwingen Sie, die ImmutabilityPolicy zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="c5aec-130">Force to remove the ImmutabilityPolicy.</span></span>

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

### <span data-ttu-id="c5aec-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5aec-131">-InputObject</span></span>
<span data-ttu-id="c5aec-132">ImmutabilityPolicy-Objekt zum Entfernen</span><span class="sxs-lookup"><span data-stu-id="c5aec-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="c5aec-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5aec-133">-ResourceGroupName</span></span>
<span data-ttu-id="c5aec-134">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="c5aec-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="c5aec-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c5aec-135">-StorageAccount</span></span>
<span data-ttu-id="c5aec-136">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="c5aec-136">Storage account object</span></span>

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

### <span data-ttu-id="c5aec-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c5aec-137">-StorageAccountName</span></span>
<span data-ttu-id="c5aec-138">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="c5aec-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="c5aec-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c5aec-139">-Confirm</span></span>
<span data-ttu-id="c5aec-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c5aec-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5aec-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5aec-141">-WhatIf</span></span>
<span data-ttu-id="c5aec-142">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c5aec-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5aec-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c5aec-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5aec-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5aec-144">CommonParameters</span></span>
<span data-ttu-id="c5aec-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5aec-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5aec-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5aec-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5aec-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c5aec-147">INPUTS</span></span>

### <span data-ttu-id="c5aec-148">System.String</span><span class="sxs-lookup"><span data-stu-id="c5aec-148">System.String</span></span>

### <span data-ttu-id="c5aec-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c5aec-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="c5aec-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="c5aec-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="c5aec-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c5aec-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="c5aec-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c5aec-152">OUTPUTS</span></span>

### <span data-ttu-id="c5aec-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c5aec-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="c5aec-154">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c5aec-154">NOTES</span></span>

## <span data-ttu-id="c5aec-155">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c5aec-155">RELATED LINKS</span></span>
