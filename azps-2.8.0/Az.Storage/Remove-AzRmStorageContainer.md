---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: d7a4563a32da28215dbb9b6dab2b911a500183a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826748"
---
# <span data-ttu-id="8ac50-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8ac50-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="8ac50-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8ac50-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac50-103">Entfernt einen BLOB-Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="8ac50-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="8ac50-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ac50-104">SYNTAX</span></span>

### <span data-ttu-id="8ac50-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="8ac50-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ac50-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="8ac50-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ac50-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="8ac50-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ac50-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ac50-108">DESCRIPTION</span></span>
<span data-ttu-id="8ac50-109">Das Cmdlet " **Remove-AzRmStorageContainer** " entfernt einen Speicher-BLOB-Container</span><span class="sxs-lookup"><span data-stu-id="8ac50-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="8ac50-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ac50-110">EXAMPLES</span></span>

### <span data-ttu-id="8ac50-111">Beispiel 1: Entfernen eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="8ac50-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="8ac50-112">Dieser Befehl entfernt einen Speicher-BLOB-Container mit dem Namen des speicherkontos und dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="8ac50-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="8ac50-113">Beispiel 2: Entfernen eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="8ac50-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="8ac50-114">Dieser Befehl entfernt einen Speicher-BLOB-Container mit dem Speicherkonto Objekt und dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="8ac50-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="8ac50-115">Beispiel 3: Entfernen aller BLOB-Speichercontainer in einem Speicherkonto mit Pipeline</span><span class="sxs-lookup"><span data-stu-id="8ac50-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="8ac50-116">Dieser Befehl entfernt alle Speicher-BLOB-Container in einem Speicherkonto mit Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8ac50-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="8ac50-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ac50-117">PARAMETERS</span></span>

### <span data-ttu-id="8ac50-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ac50-118">-DefaultProfile</span></span>
<span data-ttu-id="8ac50-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8ac50-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ac50-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8ac50-120">-Force</span></span>
<span data-ttu-id="8ac50-121">Erzwingen des Entfernens des Containers und des gesamten Inhalts</span><span class="sxs-lookup"><span data-stu-id="8ac50-121">Force to remove the container and all content in it</span></span>

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

### <span data-ttu-id="8ac50-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8ac50-122">-InputObject</span></span>
<span data-ttu-id="8ac50-123">Speichercontainer Objekt</span><span class="sxs-lookup"><span data-stu-id="8ac50-123">Storage container object</span></span>

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

### <span data-ttu-id="8ac50-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8ac50-124">-Name</span></span>
<span data-ttu-id="8ac50-125">Container Name</span><span class="sxs-lookup"><span data-stu-id="8ac50-125">Container Name</span></span>

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

### <span data-ttu-id="8ac50-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ac50-126">-PassThru</span></span>
<span data-ttu-id="8ac50-127">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="8ac50-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8ac50-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ac50-128">-ResourceGroupName</span></span>
<span data-ttu-id="8ac50-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8ac50-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="8ac50-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ac50-130">-StorageAccount</span></span>
<span data-ttu-id="8ac50-131">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="8ac50-131">Storage account object</span></span>

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

### <span data-ttu-id="8ac50-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8ac50-132">-StorageAccountName</span></span>
<span data-ttu-id="8ac50-133">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="8ac50-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="8ac50-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8ac50-134">-Confirm</span></span>
<span data-ttu-id="8ac50-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8ac50-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ac50-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ac50-136">-WhatIf</span></span>
<span data-ttu-id="8ac50-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8ac50-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ac50-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ac50-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ac50-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac50-139">CommonParameters</span></span>
<span data-ttu-id="8ac50-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ac50-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac50-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ac50-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac50-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8ac50-142">INPUTS</span></span>

### <span data-ttu-id="8ac50-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8ac50-143">System.String</span></span>

### <span data-ttu-id="8ac50-144">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ac50-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="8ac50-145">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="8ac50-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="8ac50-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8ac50-146">OUTPUTS</span></span>

### <span data-ttu-id="8ac50-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8ac50-147">System.Boolean</span></span>

## <span data-ttu-id="8ac50-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="8ac50-148">NOTES</span></span>

## <span data-ttu-id="8ac50-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8ac50-149">RELATED LINKS</span></span>
