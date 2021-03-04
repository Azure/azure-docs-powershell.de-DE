---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: 467fab7d2d7c344c3ffa2ca631addb538e790101
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937283"
---
# <span data-ttu-id="1cc57-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1cc57-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="1cc57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cc57-102">SYNOPSIS</span></span>
<span data-ttu-id="1cc57-103">Entfernt einen Speicherblobcontainer</span><span class="sxs-lookup"><span data-stu-id="1cc57-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="1cc57-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1cc57-104">SYNTAX</span></span>

### <span data-ttu-id="1cc57-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="1cc57-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cc57-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="1cc57-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cc57-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="1cc57-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cc57-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1cc57-108">DESCRIPTION</span></span>
<span data-ttu-id="1cc57-109">Das **Cmdlet Remove-AzRmStorageContainer** entfernt einen Speicherblobcontainer.</span><span class="sxs-lookup"><span data-stu-id="1cc57-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="1cc57-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1cc57-110">EXAMPLES</span></span>

### <span data-ttu-id="1cc57-111">Beispiel 1: Entfernen eines Speicherblobscontainers mit Dem Namen des Speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="1cc57-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="1cc57-112">Mit diesem Befehl wird ein Speicherblobcontainer mit dem Namen des Speicherkontos und dem Containernamen entfernt.</span><span class="sxs-lookup"><span data-stu-id="1cc57-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="1cc57-113">Beispiel 2: Entfernen eines Speicherblobscontainers mit Speicherkontoobjekt und Containername</span><span class="sxs-lookup"><span data-stu-id="1cc57-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="1cc57-114">Mit diesem Befehl wird ein Speicherblobcontainer mit Speicherkontoobjekt und Containername entfernt.</span><span class="sxs-lookup"><span data-stu-id="1cc57-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="1cc57-115">Beispiel 3: Entfernen aller Speicherblobcontainer in einem Speicherkonto mit Pipeline</span><span class="sxs-lookup"><span data-stu-id="1cc57-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="1cc57-116">Mit diesem Befehl werden alle Speicherblobcontainer in einem Speicherkonto mit Pipeline entfernt.</span><span class="sxs-lookup"><span data-stu-id="1cc57-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="1cc57-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1cc57-117">PARAMETERS</span></span>

### <span data-ttu-id="1cc57-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cc57-118">-DefaultProfile</span></span>
<span data-ttu-id="1cc57-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1cc57-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cc57-120">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="1cc57-120">-Force</span></span>
<span data-ttu-id="1cc57-121">Erzwingen des Entfernens des Containers und aller Inhalte in diesem Container</span><span class="sxs-lookup"><span data-stu-id="1cc57-121">Force to remove the container and all content in it</span></span>

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

### <span data-ttu-id="1cc57-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1cc57-122">-InputObject</span></span>
<span data-ttu-id="1cc57-123">Speichercontainerobjekt</span><span class="sxs-lookup"><span data-stu-id="1cc57-123">Storage container object</span></span>

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

### <span data-ttu-id="1cc57-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1cc57-124">-Name</span></span>
<span data-ttu-id="1cc57-125">Containername</span><span class="sxs-lookup"><span data-stu-id="1cc57-125">Container Name</span></span>

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

### <span data-ttu-id="1cc57-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1cc57-126">-PassThru</span></span>
<span data-ttu-id="1cc57-127">Gibt an, dass dieses Cmdlet einen **booleschen** Wert zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="1cc57-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="1cc57-128">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1cc57-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="1cc57-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cc57-129">-ResourceGroupName</span></span>
<span data-ttu-id="1cc57-130">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="1cc57-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="1cc57-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="1cc57-131">-StorageAccount</span></span>
<span data-ttu-id="1cc57-132">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="1cc57-132">Storage account object</span></span>

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

### <span data-ttu-id="1cc57-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1cc57-133">-StorageAccountName</span></span>
<span data-ttu-id="1cc57-134">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="1cc57-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="1cc57-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1cc57-135">-Confirm</span></span>
<span data-ttu-id="1cc57-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1cc57-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cc57-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cc57-137">-WhatIf</span></span>
<span data-ttu-id="1cc57-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1cc57-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1cc57-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1cc57-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cc57-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cc57-140">CommonParameters</span></span>
<span data-ttu-id="1cc57-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cc57-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cc57-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cc57-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cc57-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1cc57-143">INPUTS</span></span>

### <span data-ttu-id="1cc57-144">System.String</span><span class="sxs-lookup"><span data-stu-id="1cc57-144">System.String</span></span>

### <span data-ttu-id="1cc57-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1cc57-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="1cc57-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="1cc57-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="1cc57-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1cc57-147">OUTPUTS</span></span>

### <span data-ttu-id="1cc57-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1cc57-148">System.Boolean</span></span>

## <span data-ttu-id="1cc57-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1cc57-149">NOTES</span></span>

## <span data-ttu-id="1cc57-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1cc57-150">RELATED LINKS</span></span>
