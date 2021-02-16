---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: 333df1432ed892e75e0b798f1412cb7b0327a334
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158041"
---
# <span data-ttu-id="c48c2-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c48c2-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="c48c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c48c2-102">SYNOPSIS</span></span>
<span data-ttu-id="c48c2-103">Entfernt einen Speicher-BLOB-Container.</span><span class="sxs-lookup"><span data-stu-id="c48c2-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="c48c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c48c2-104">SYNTAX</span></span>

### <span data-ttu-id="c48c2-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c48c2-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c48c2-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="c48c2-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c48c2-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="c48c2-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c48c2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c48c2-108">DESCRIPTION</span></span>
<span data-ttu-id="c48c2-109">Das **Cmdlet "Remove-AzRmStorageContainer"** entfernt einen Speicher-BLOB-Container.</span><span class="sxs-lookup"><span data-stu-id="c48c2-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="c48c2-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c48c2-110">EXAMPLES</span></span>

### <span data-ttu-id="c48c2-111">Beispiel 1: Entfernen eines Speicher-BLOB-Containers mit dem Namen des Speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="c48c2-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="c48c2-112">Mit diesem Befehl wird ein Speicher-BLOB-Container mit dem Namen des Speicherkontos und dem Containernamen entfernt.</span><span class="sxs-lookup"><span data-stu-id="c48c2-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="c48c2-113">Beispiel 2: Entfernen eines Speicher-BLOB-Containers mit Speicherkontoobjekt und Containername</span><span class="sxs-lookup"><span data-stu-id="c48c2-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="c48c2-114">Mit diesem Befehl wird ein Speicher-BLOB-Container mit speicherkontoobjekt und Containername entfernt.</span><span class="sxs-lookup"><span data-stu-id="c48c2-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="c48c2-115">Beispiel 3: Entfernen aller Speicher-BLOB-Container in einem Speicherkonto mit Pipeline</span><span class="sxs-lookup"><span data-stu-id="c48c2-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="c48c2-116">Mit diesem Befehl werden alle Speicher-BLOB-Container in einem Speicherkonto mit Pipeline entfernt.</span><span class="sxs-lookup"><span data-stu-id="c48c2-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="c48c2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c48c2-117">PARAMETERS</span></span>

### <span data-ttu-id="c48c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c48c2-118">-DefaultProfile</span></span>
<span data-ttu-id="c48c2-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c48c2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c48c2-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c48c2-120">-Force</span></span>
<span data-ttu-id="c48c2-121">Erzwingen des Entfernens des Containers und des sämtlichen Inhalts</span><span class="sxs-lookup"><span data-stu-id="c48c2-121">Force to remove the container and all content in it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c48c2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c48c2-122">-InputObject</span></span>
<span data-ttu-id="c48c2-123">Speichercontainerobjekt</span><span class="sxs-lookup"><span data-stu-id="c48c2-123">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c48c2-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c48c2-124">-Name</span></span>
<span data-ttu-id="c48c2-125">Containername</span><span class="sxs-lookup"><span data-stu-id="c48c2-125">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c48c2-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c48c2-126">-PassThru</span></span>
<span data-ttu-id="c48c2-127">Gibt an, dass dieses Cmdlet einen **booleschen** Wert zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="c48c2-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="c48c2-128">Dieses Cmdlet gibt standardmäßig keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c48c2-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="c48c2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c48c2-129">-ResourceGroupName</span></span>
<span data-ttu-id="c48c2-130">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="c48c2-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="c48c2-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c48c2-131">-StorageAccount</span></span>
<span data-ttu-id="c48c2-132">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="c48c2-132">Storage account object</span></span>

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

### <span data-ttu-id="c48c2-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c48c2-133">-StorageAccountName</span></span>
<span data-ttu-id="c48c2-134">Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="c48c2-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="c48c2-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c48c2-135">-Confirm</span></span>
<span data-ttu-id="c48c2-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c48c2-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c48c2-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c48c2-137">-WhatIf</span></span>
<span data-ttu-id="c48c2-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c48c2-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c48c2-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c48c2-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c48c2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c48c2-140">CommonParameters</span></span>
<span data-ttu-id="c48c2-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c48c2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c48c2-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c48c2-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c48c2-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c48c2-143">INPUTS</span></span>

### <span data-ttu-id="c48c2-144">System.String</span><span class="sxs-lookup"><span data-stu-id="c48c2-144">System.String</span></span>

### <span data-ttu-id="c48c2-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c48c2-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="c48c2-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="c48c2-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="c48c2-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c48c2-147">OUTPUTS</span></span>

### <span data-ttu-id="c48c2-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c48c2-148">System.Boolean</span></span>

## <span data-ttu-id="c48c2-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c48c2-149">NOTES</span></span>

## <span data-ttu-id="c48c2-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c48c2-150">RELATED LINKS</span></span>
