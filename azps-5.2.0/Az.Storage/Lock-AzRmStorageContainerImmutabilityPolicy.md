---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/lock-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 0cb3a4e65d8e464dda85e18e12dc106620e3eee8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304139"
---
# <span data-ttu-id="fc8e6-101">Lock-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="fc8e6-101">Lock-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="fc8e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc8e6-102">SYNOPSIS</span></span>
<span data-ttu-id="fc8e6-103">Sperrt ImmutabilityPolicy eines Speicher-BLOB-Containers</span><span class="sxs-lookup"><span data-stu-id="fc8e6-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="fc8e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc8e6-104">SYNTAX</span></span>

### <span data-ttu-id="fc8e6-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fc8e6-105">AccountName (Default)</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc8e6-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="fc8e6-106">AccountObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc8e6-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="fc8e6-107">ContainerObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc8e6-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="fc8e6-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc8e6-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc8e6-109">DESCRIPTION</span></span>
<span data-ttu-id="fc8e6-110">Das **Cmdlet "Lock-AzRmStorageContainerImmutabilityPolicy"** sperrt ImmutabilityPolicy eines Speicher-BLOB-Containers.</span><span class="sxs-lookup"><span data-stu-id="fc8e6-110">The **Lock-AzRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="fc8e6-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fc8e6-111">EXAMPLES</span></span>

### <span data-ttu-id="fc8e6-112">Beispiel 1: Sperren von ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Namen des Speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="fc8e6-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="fc8e6-113">Mit diesem Befehl wird "ImmutabilityPolicy" eines Speicher-BLOB-Containers mit dem Namen des Speicherkontos und dem Containernamen gesperrt.</span><span class="sxs-lookup"><span data-stu-id="fc8e6-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="fc8e6-114">Beispiel 2: Sperren von ImmutabilityPolicy eines Speicher-BLOB-Containers mit Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="fc8e6-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="fc8e6-115">Mit diesem Befehl wird "ImmutabilityPolicy" eines Speicher-BLOB-Containers mit speicherkontoobjekt gesperrt.</span><span class="sxs-lookup"><span data-stu-id="fc8e6-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="fc8e6-116">Beispiel 3: Sperren von ImmutabilityPolicyof eines Speicher-BLOB-Containers mit Containerobjekt</span><span class="sxs-lookup"><span data-stu-id="fc8e6-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="fc8e6-117">Mit diesem Befehl wird "ImmutabilityPolicy" eines Speicher-BLOB-Containers mit einem Speichercontainerobjekt gesperrt.</span><span class="sxs-lookup"><span data-stu-id="fc8e6-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="fc8e6-118">Beispiel 4: Sperren von ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem ImmutabilityPolicy-Objekt</span><span class="sxs-lookup"><span data-stu-id="fc8e6-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="fc8e6-119">Mit diesem Befehl wird "ImmutabilityPolicy" eines Speicher-BLOB-Containers mit dem ImmutabilityPolicy-Objekt gesperrt.</span><span class="sxs-lookup"><span data-stu-id="fc8e6-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="fc8e6-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc8e6-120">PARAMETERS</span></span>

### <span data-ttu-id="fc8e6-121">-Container</span><span class="sxs-lookup"><span data-stu-id="fc8e6-121">-Container</span></span>
<span data-ttu-id="fc8e6-122">Speichercontainerobjekt</span><span class="sxs-lookup"><span data-stu-id="fc8e6-122">Storage container object</span></span>

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

### <span data-ttu-id="fc8e6-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="fc8e6-123">-ContainerName</span></span>
<span data-ttu-id="fc8e6-124">Containername</span><span class="sxs-lookup"><span data-stu-id="fc8e6-124">Container Name</span></span>

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

### <span data-ttu-id="fc8e6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc8e6-125">-DefaultProfile</span></span>
<span data-ttu-id="fc8e6-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc8e6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc8e6-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="fc8e6-127">-Etag</span></span>
<span data-ttu-id="fc8e6-128">E-Tag der Immutbarkeitsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="fc8e6-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="fc8e6-129">-Force</span><span class="sxs-lookup"><span data-stu-id="fc8e6-129">-Force</span></span>
<span data-ttu-id="fc8e6-130">Erzwingen Sie das Entfernen von "ImmutabilityPolicy".</span><span class="sxs-lookup"><span data-stu-id="fc8e6-130">Force to remove the ImmutabilityPolicy.</span></span>

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

### <span data-ttu-id="fc8e6-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc8e6-131">-InputObject</span></span>
<span data-ttu-id="fc8e6-132">ImmutabilityPolicy-Objekt, das entfernt werden soll</span><span class="sxs-lookup"><span data-stu-id="fc8e6-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="fc8e6-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc8e6-133">-ResourceGroupName</span></span>
<span data-ttu-id="fc8e6-134">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="fc8e6-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="fc8e6-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="fc8e6-135">-StorageAccount</span></span>
<span data-ttu-id="fc8e6-136">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="fc8e6-136">Storage account object</span></span>

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

### <span data-ttu-id="fc8e6-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fc8e6-137">-StorageAccountName</span></span>
<span data-ttu-id="fc8e6-138">Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="fc8e6-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="fc8e6-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc8e6-139">-Confirm</span></span>
<span data-ttu-id="fc8e6-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fc8e6-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc8e6-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fc8e6-141">-WhatIf</span></span>
<span data-ttu-id="fc8e6-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc8e6-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc8e6-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc8e6-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc8e6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc8e6-144">CommonParameters</span></span>
<span data-ttu-id="fc8e6-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc8e6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc8e6-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc8e6-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc8e6-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fc8e6-147">INPUTS</span></span>

### <span data-ttu-id="fc8e6-148">System.String</span><span class="sxs-lookup"><span data-stu-id="fc8e6-148">System.String</span></span>

### <span data-ttu-id="fc8e6-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fc8e6-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="fc8e6-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="fc8e6-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="fc8e6-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="fc8e6-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="fc8e6-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fc8e6-152">OUTPUTS</span></span>

### <span data-ttu-id="fc8e6-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="fc8e6-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="fc8e6-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fc8e6-154">NOTES</span></span>

## <span data-ttu-id="fc8e6-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fc8e6-155">RELATED LINKS</span></span>
