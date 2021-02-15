---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
ms.openlocfilehash: bff7a79513cc8eb0047860f9edd00c6c37c5f1b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158017"
---
# <span data-ttu-id="5e343-101">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5e343-101">Remove-AzRmStorageShare</span></span>

## <span data-ttu-id="5e343-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e343-102">SYNOPSIS</span></span>
<span data-ttu-id="5e343-103">Entfernt eine Speicherdateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="5e343-103">Removes a Storage file share.</span></span>

## <span data-ttu-id="5e343-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e343-104">SYNTAX</span></span>

### <span data-ttu-id="5e343-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e343-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e343-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="5e343-106">AccountObject</span></span>
```
Remove-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e343-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="5e343-107">ShareResourceId</span></span>
```
Remove-AzRmStorageShare [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e343-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="5e343-108">ShareObject</span></span>
```
Remove-AzRmStorageShare -InputObject <PSShare> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e343-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e343-109">DESCRIPTION</span></span>
<span data-ttu-id="5e343-110">Das **Cmdlet "New-AzRmStorageShare"** entfernt eine Speicherdateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="5e343-110">The **New-AzRmStorageShare** cmdlet removes a Storage file share.</span></span>

## <span data-ttu-id="5e343-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5e343-111">EXAMPLES</span></span>

### <span data-ttu-id="5e343-112">Beispiel 1: Entfernen einer Speicherdateifreigabe mit dem Namen des Speicherkontos und dem Freigabenamen</span><span class="sxs-lookup"><span data-stu-id="5e343-112">Example 1: Remove a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Remove-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"
```

<span data-ttu-id="5e343-113">Mit diesem Befehl wird eine Speicherdateifreigabe mit dem Namen des Speicherkontos und dem Freigabenamen entfernt.</span><span class="sxs-lookup"><span data-stu-id="5e343-113">This command removes a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="5e343-114">Beispiel 2: Entfernen einer Speicherdateifreigabe mit Speicherkontoobjekt und Freigabename</span><span class="sxs-lookup"><span data-stu-id="5e343-114">Example 2: Remove a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageShare -StorageAccount $accountObject -Name "myshare"
```

<span data-ttu-id="5e343-115">Mit diesem Befehl wird eine Speicherdateifreigabe mit dem Objekt "Speicherkonto" und dem Freigabenamen entfernt.</span><span class="sxs-lookup"><span data-stu-id="5e343-115">This command removes a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="5e343-116">Beispiel 3: Entfernen aller Speicherdateifreigaben in einem Speicherkonto mit Pipeline</span><span class="sxs-lookup"><span data-stu-id="5e343-116">Example 3: Remove all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Remove-AzRmStorageShare -Force
```

<span data-ttu-id="5e343-117">Mit diesem Befehl werden alle Speicherdateifreigaben in einem Speicherkonto mit Pipeline entfernt.</span><span class="sxs-lookup"><span data-stu-id="5e343-117">This command removes all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="5e343-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e343-118">PARAMETERS</span></span>

### <span data-ttu-id="5e343-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e343-119">-DefaultProfile</span></span>
<span data-ttu-id="5e343-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e343-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e343-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5e343-121">-Force</span></span>
<span data-ttu-id="5e343-122">Erzwingen des Entfernens der Freigabe und aller Inhalte</span><span class="sxs-lookup"><span data-stu-id="5e343-122">Force to remove the Share and all content in it</span></span>

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

### <span data-ttu-id="5e343-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e343-123">-InputObject</span></span>
<span data-ttu-id="5e343-124">Speicherfreigabeobjekt</span><span class="sxs-lookup"><span data-stu-id="5e343-124">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e343-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5e343-125">-Name</span></span>
<span data-ttu-id="5e343-126">Freigabename</span><span class="sxs-lookup"><span data-stu-id="5e343-126">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e343-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e343-127">-PassThru</span></span>
<span data-ttu-id="5e343-128">Gibt an, dass dieses Cmdlet einen **booleschen** Wert zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="5e343-128">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="5e343-129">Dieses Cmdlet gibt standardmäßig keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5e343-129">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="5e343-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e343-130">-ResourceGroupName</span></span>
<span data-ttu-id="5e343-131">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="5e343-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e343-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e343-132">-ResourceId</span></span>
<span data-ttu-id="5e343-133">Geben Sie eine Dateifreigaberessourcen-ID ein.</span><span class="sxs-lookup"><span data-stu-id="5e343-133">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e343-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="5e343-134">-StorageAccount</span></span>
<span data-ttu-id="5e343-135">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="5e343-135">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e343-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5e343-136">-StorageAccountName</span></span>
<span data-ttu-id="5e343-137">Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="5e343-137">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e343-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e343-138">-Confirm</span></span>
<span data-ttu-id="5e343-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e343-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e343-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5e343-140">-WhatIf</span></span>
<span data-ttu-id="5e343-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e343-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e343-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e343-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e343-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e343-143">CommonParameters</span></span>
<span data-ttu-id="5e343-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e343-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e343-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e343-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e343-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5e343-146">INPUTS</span></span>

### <span data-ttu-id="5e343-147">System.String</span><span class="sxs-lookup"><span data-stu-id="5e343-147">System.String</span></span>

### <span data-ttu-id="5e343-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5e343-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="5e343-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="5e343-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="5e343-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5e343-150">OUTPUTS</span></span>

### <span data-ttu-id="5e343-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5e343-151">System.Boolean</span></span>

## <span data-ttu-id="5e343-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5e343-152">NOTES</span></span>

## <span data-ttu-id="5e343-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5e343-153">RELATED LINKS</span></span>
