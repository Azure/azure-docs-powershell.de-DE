---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 494995a97ccb74df9ad9a9fc1f88272505598bb9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173389"
---
# <span data-ttu-id="8b8ee-101">Remove-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="8b8ee-101">Remove-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="8b8ee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b8ee-102">SYNOPSIS</span></span>
<span data-ttu-id="8b8ee-103">Entfernt zulässige Aufbewahrungstags aus einem BLOB-Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="8b8ee-103">Removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="8b8ee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b8ee-104">SYNTAX</span></span>

### <span data-ttu-id="8b8ee-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="8b8ee-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b8ee-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="8b8ee-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b8ee-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="8b8ee-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b8ee-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b8ee-108">DESCRIPTION</span></span>
<span data-ttu-id="8b8ee-109">Das Cmdlet **Remove-AzRmStorageContainerLegalHold** entfernt zulässige Aufbewahrungstags aus einem BLOB-Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="8b8ee-109">The **Remove-AzRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="8b8ee-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b8ee-110">EXAMPLES</span></span>

### <span data-ttu-id="8b8ee-111">Beispiel 1: Entfernen von gültigen Aufbewahrungstags aus einem BLOB-Speichercontainer mit dem Namen des speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="8b8ee-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="8b8ee-112">Mit diesem Befehl werden zulässige Aufbewahrungstags aus einem BLOB-Speichercontainer mit Speicherkonto Name und Containernamen entfernt.</span><span class="sxs-lookup"><span data-stu-id="8b8ee-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="8b8ee-113">Beispiel 2: Entfernen von gültigen Aufbewahrungstags aus einem BLOB-Speichercontainer mit Speicherkonto Objekt und Containernamen</span><span class="sxs-lookup"><span data-stu-id="8b8ee-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2
```

<span data-ttu-id="8b8ee-114">Mit diesem Befehl werden zulässige Aufbewahrungstags aus einem BLOB-Speichercontainer mit dem Speicherkonto Objekt und dem Containernamen entfernt.</span><span class="sxs-lookup"><span data-stu-id="8b8ee-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="8b8ee-115">Beispiel 3: Entfernen von gültigen Aufbewahrungstags aus allen BLOB-Speicher Containern in einem Speicherkonto mit Pipeline</span><span class="sxs-lookup"><span data-stu-id="8b8ee-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="8b8ee-116">Dieser Befehl entfernt zulässige Aufbewahrungstags aus allen BLOB-Speicher Containern in einem Speicherkonto mit Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8b8ee-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="8b8ee-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b8ee-117">PARAMETERS</span></span>

### <span data-ttu-id="8b8ee-118">-Container</span><span class="sxs-lookup"><span data-stu-id="8b8ee-118">-Container</span></span>
<span data-ttu-id="8b8ee-119">Speichercontainer Objekt</span><span class="sxs-lookup"><span data-stu-id="8b8ee-119">Storage container object</span></span>

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

### <span data-ttu-id="8b8ee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b8ee-120">-DefaultProfile</span></span>
<span data-ttu-id="8b8ee-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8b8ee-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b8ee-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8b8ee-122">-Name</span></span>
<span data-ttu-id="8b8ee-123">Container Name</span><span class="sxs-lookup"><span data-stu-id="8b8ee-123">Container Name</span></span>

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

### <span data-ttu-id="8b8ee-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b8ee-124">-ResourceGroupName</span></span>
<span data-ttu-id="8b8ee-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8b8ee-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="8b8ee-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b8ee-126">-StorageAccount</span></span>
<span data-ttu-id="8b8ee-127">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="8b8ee-127">Storage account object</span></span>

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

### <span data-ttu-id="8b8ee-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8b8ee-128">-StorageAccountName</span></span>
<span data-ttu-id="8b8ee-129">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="8b8ee-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="8b8ee-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="8b8ee-130">-Tag</span></span>
<span data-ttu-id="8b8ee-131">Container-LegalHold-Tags</span><span class="sxs-lookup"><span data-stu-id="8b8ee-131">Container LegalHold Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b8ee-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8b8ee-132">-Confirm</span></span>
<span data-ttu-id="8b8ee-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8b8ee-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b8ee-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b8ee-134">-WhatIf</span></span>
<span data-ttu-id="8b8ee-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b8ee-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b8ee-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b8ee-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b8ee-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b8ee-137">CommonParameters</span></span>
<span data-ttu-id="8b8ee-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b8ee-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b8ee-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b8ee-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b8ee-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b8ee-140">INPUTS</span></span>

### <span data-ttu-id="8b8ee-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8b8ee-141">System.String</span></span>

### <span data-ttu-id="8b8ee-142">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b8ee-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="8b8ee-143">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="8b8ee-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="8b8ee-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b8ee-144">OUTPUTS</span></span>

### <span data-ttu-id="8b8ee-145">Microsoft. Azure. Commands. Management. Storage. Models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="8b8ee-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="8b8ee-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b8ee-146">NOTES</span></span>

## <span data-ttu-id="8b8ee-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b8ee-147">RELATED LINKS</span></span>
