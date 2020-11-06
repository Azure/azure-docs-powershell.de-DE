---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/add-azurermstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageContainerLegalHold.md
ms.openlocfilehash: 465a40e384e5ea7240e0ced2a010c88529feb2f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477617"
---
# <span data-ttu-id="8e8d7-101">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="8e8d7-101">Add-AzureRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="8e8d7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8e8d7-102">SYNOPSIS</span></span>
<span data-ttu-id="8e8d7-103">Fügt einem Speicher-BLOB-Container rechtliche Aufbewahrungstags hinzu</span><span class="sxs-lookup"><span data-stu-id="8e8d7-103">Adds legal hold tags to a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e8d7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e8d7-104">SYNTAX</span></span>

### <span data-ttu-id="8e8d7-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e8d7-105">AccountName (Default)</span></span>
```
Add-AzureRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e8d7-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="8e8d7-106">AccountObject</span></span>
```
Add-AzureRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e8d7-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="8e8d7-107">ContainerObject</span></span>
```
Add-AzureRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e8d7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e8d7-108">DESCRIPTION</span></span>
<span data-ttu-id="8e8d7-109">Das **Add-AzureRmStorageContainerLegalHold-** Cmdlet fügt einem Speicher-BLOB-Container rechtliche Aufbewahrungstags hinzu.</span><span class="sxs-lookup"><span data-stu-id="8e8d7-109">The **Add-AzureRmStorageContainerLegalHold** cmdlet adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="8e8d7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e8d7-110">EXAMPLES</span></span>

### <span data-ttu-id="8e8d7-111">Beispiel 1: Hinzufügen von gültigen Aufbewahrungstags zu einem BLOB-Speichercontainer mit dem Namen des speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="8e8d7-111">Example 1: Add legal hold tags to a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Add-AzureRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2 
```

<span data-ttu-id="8e8d7-112">Dieser Befehl fügt einem Speicher-BLOB-Container mit dem Namen des speicherkontos und dem Containernamen zulässige Aufbewahrungstags hinzu.</span><span class="sxs-lookup"><span data-stu-id="8e8d7-112">This command adds legal hold tags to a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="8e8d7-113">Beispiel 2: Hinzufügen von gültigen Aufbewahrungstags zu einem BLOB-Speichercontainer mit Speicherkonto Objekt und Containernamen</span><span class="sxs-lookup"><span data-stu-id="8e8d7-113">Example 2: Add legal hold tags to a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzureRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

<span data-ttu-id="8e8d7-114">Dieser Befehl fügt einem Speicher-BLOB-Container mit dem Speicherkonto Objekt und dem Containernamen zulässige Aufbewahrungstags hinzu.</span><span class="sxs-lookup"><span data-stu-id="8e8d7-114">This command adds legal hold tags to a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="8e8d7-115">Beispiel 3: Hinzufügen von gültigen Aufbewahrungstags zu allen BLOB-Speicher Containern in einem Speicherkonto mit Pipeline</span><span class="sxs-lookup"><span data-stu-id="8e8d7-115">Example 3: Add legal hold tags to all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzureRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

<span data-ttu-id="8e8d7-116">Dieser Befehl fügt allen Speicher-BLOB-Containern in einem Speicherkonto mit Pipeline zugelassene Aufbewahrungstags hinzu.</span><span class="sxs-lookup"><span data-stu-id="8e8d7-116">This command adds legal hold tags to all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="8e8d7-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e8d7-117">PARAMETERS</span></span>

### <span data-ttu-id="8e8d7-118">-Container</span><span class="sxs-lookup"><span data-stu-id="8e8d7-118">-Container</span></span>
<span data-ttu-id="8e8d7-119">Speichercontainer Objekt</span><span class="sxs-lookup"><span data-stu-id="8e8d7-119">Storage container object</span></span>

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

### <span data-ttu-id="8e8d7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e8d7-120">-DefaultProfile</span></span>
<span data-ttu-id="8e8d7-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e8d7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e8d7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8e8d7-122">-Name</span></span>
<span data-ttu-id="8e8d7-123">Container Name</span><span class="sxs-lookup"><span data-stu-id="8e8d7-123">Container Name</span></span>

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

### <span data-ttu-id="8e8d7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e8d7-124">-ResourceGroupName</span></span>
<span data-ttu-id="8e8d7-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8e8d7-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="8e8d7-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e8d7-126">-StorageAccount</span></span>
<span data-ttu-id="8e8d7-127">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="8e8d7-127">Storage account object</span></span>

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

### <span data-ttu-id="8e8d7-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8e8d7-128">-StorageAccountName</span></span>
<span data-ttu-id="8e8d7-129">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="8e8d7-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="8e8d7-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="8e8d7-130">-Tag</span></span>
<span data-ttu-id="8e8d7-131">Container-LegalHold-Tags</span><span class="sxs-lookup"><span data-stu-id="8e8d7-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="8e8d7-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8e8d7-132">-Confirm</span></span>
<span data-ttu-id="8e8d7-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e8d7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e8d7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e8d7-134">-WhatIf</span></span>
<span data-ttu-id="8e8d7-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e8d7-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e8d7-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e8d7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e8d7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e8d7-137">CommonParameters</span></span>
<span data-ttu-id="8e8d7-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e8d7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e8d7-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e8d7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e8d7-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8e8d7-140">INPUTS</span></span>

### <span data-ttu-id="8e8d7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8e8d7-141">System.String</span></span>

## <span data-ttu-id="8e8d7-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8e8d7-142">OUTPUTS</span></span>

### <span data-ttu-id="8e8d7-143">Microsoft. Azure. Commands. Management. Storage. Models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="8e8d7-143">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="8e8d7-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="8e8d7-144">NOTES</span></span>

## <span data-ttu-id="8e8d7-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8e8d7-145">RELATED LINKS</span></span>

