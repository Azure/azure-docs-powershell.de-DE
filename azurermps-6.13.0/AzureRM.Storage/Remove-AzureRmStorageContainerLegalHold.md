---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerLegalHold.md
ms.openlocfilehash: da0793e7eb10f7b83d785aea34866842abe9b887
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498157"
---
# <span data-ttu-id="4185b-101">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="4185b-101">Remove-AzureRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="4185b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4185b-102">SYNOPSIS</span></span>
<span data-ttu-id="4185b-103">Entfernt zulässige Aufbewahrungstags aus einem BLOB-Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="4185b-103">Removes legal hold tags from a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4185b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4185b-104">SYNTAX</span></span>

### <span data-ttu-id="4185b-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="4185b-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4185b-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="4185b-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4185b-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="4185b-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4185b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4185b-108">DESCRIPTION</span></span>
<span data-ttu-id="4185b-109">Das Cmdlet **Remove-AzureRmStorageContainerLegalHold** entfernt zulässige Aufbewahrungstags aus einem BLOB-Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="4185b-109">The **Remove-AzureRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="4185b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4185b-110">EXAMPLES</span></span>

### <span data-ttu-id="4185b-111">Beispiel 1: Entfernen von gültigen Aufbewahrungstags aus einem BLOB-Speichercontainer mit dem Namen des speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="4185b-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzureRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="4185b-112">Mit diesem Befehl werden zulässige Aufbewahrungstags aus einem BLOB-Speichercontainer mit Speicherkonto Name und Containernamen entfernt.</span><span class="sxs-lookup"><span data-stu-id="4185b-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="4185b-113">Beispiel 2: Entfernen von gültigen Aufbewahrungstags aus einem BLOB-Speichercontainer mit Speicherkonto Objekt und Containernamen</span><span class="sxs-lookup"><span data-stu-id="4185b-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzureRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2 
```

<span data-ttu-id="4185b-114">Mit diesem Befehl werden zulässige Aufbewahrungstags aus einem BLOB-Speichercontainer mit dem Speicherkonto Objekt und dem Containernamen entfernt.</span><span class="sxs-lookup"><span data-stu-id="4185b-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="4185b-115">Beispiel 3: Entfernen von gültigen Aufbewahrungstags aus allen BLOB-Speicher Containern in einem Speicherkonto mit Pipeline</span><span class="sxs-lookup"><span data-stu-id="4185b-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzureRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="4185b-116">Dieser Befehl entfernt zulässige Aufbewahrungstags aus allen BLOB-Speicher Containern in einem Speicherkonto mit Pipeline.</span><span class="sxs-lookup"><span data-stu-id="4185b-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>


## <span data-ttu-id="4185b-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="4185b-117">PARAMETERS</span></span>

### <span data-ttu-id="4185b-118">-Container</span><span class="sxs-lookup"><span data-stu-id="4185b-118">-Container</span></span>
<span data-ttu-id="4185b-119">Speichercontainer Objekt</span><span class="sxs-lookup"><span data-stu-id="4185b-119">Storage container object</span></span>

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

### <span data-ttu-id="4185b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4185b-120">-DefaultProfile</span></span>
<span data-ttu-id="4185b-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4185b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4185b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4185b-122">-Name</span></span>
<span data-ttu-id="4185b-123">Container Name</span><span class="sxs-lookup"><span data-stu-id="4185b-123">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4185b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4185b-124">-ResourceGroupName</span></span>
<span data-ttu-id="4185b-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4185b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="4185b-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="4185b-126">-StorageAccount</span></span>
<span data-ttu-id="4185b-127">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="4185b-127">Storage account object</span></span>

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

### <span data-ttu-id="4185b-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4185b-128">-StorageAccountName</span></span>
<span data-ttu-id="4185b-129">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="4185b-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="4185b-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="4185b-130">-Tag</span></span>
<span data-ttu-id="4185b-131">Container-LegalHold-Tags</span><span class="sxs-lookup"><span data-stu-id="4185b-131">Container LegalHold Tags</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185b-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4185b-132">-Confirm</span></span>
<span data-ttu-id="4185b-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4185b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4185b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4185b-134">-WhatIf</span></span>
<span data-ttu-id="4185b-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4185b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4185b-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4185b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4185b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4185b-137">CommonParameters</span></span>
<span data-ttu-id="4185b-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4185b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4185b-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4185b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4185b-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4185b-140">INPUTS</span></span>

### <span data-ttu-id="4185b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4185b-141">System.String</span></span>

## <span data-ttu-id="4185b-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4185b-142">OUTPUTS</span></span>

### <span data-ttu-id="4185b-143">Microsoft. Azure. Commands. Management. Storage. Models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="4185b-143">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="4185b-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="4185b-144">NOTES</span></span>

## <span data-ttu-id="4185b-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4185b-145">RELATED LINKS</span></span>

