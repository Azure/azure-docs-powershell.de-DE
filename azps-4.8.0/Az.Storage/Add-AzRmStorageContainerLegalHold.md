---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 438aa207d28ca2a432d413f847d674d25bf55a42
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010422"
---
# <span data-ttu-id="9cbed-101">Add-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="9cbed-101">Add-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="9cbed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9cbed-102">SYNOPSIS</span></span>
<span data-ttu-id="9cbed-103">Fügt einem Speicher-BLOB-Container rechtliche Aufbewahrungstags hinzu</span><span class="sxs-lookup"><span data-stu-id="9cbed-103">Adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="9cbed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cbed-104">SYNTAX</span></span>

### <span data-ttu-id="9cbed-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="9cbed-105">AccountName (Default)</span></span>
```
Add-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cbed-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="9cbed-106">AccountObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cbed-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="9cbed-107">ContainerObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cbed-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9cbed-108">DESCRIPTION</span></span>
<span data-ttu-id="9cbed-109">Das **Add-AzRmStorageContainerLegalHold-** Cmdlet fügt einem Speicher-BLOB-Container rechtliche Aufbewahrungstags hinzu.</span><span class="sxs-lookup"><span data-stu-id="9cbed-109">The **Add-AzRmStorageContainerLegalHold** cmdlet adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="9cbed-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9cbed-110">EXAMPLES</span></span>

### <span data-ttu-id="9cbed-111">Beispiel 1: Hinzufügen von gültigen Aufbewahrungstags zu einem BLOB-Speichercontainer mit dem Namen des speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="9cbed-111">Example 1: Add legal hold tags to a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Add-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2
```

<span data-ttu-id="9cbed-112">Dieser Befehl fügt einem Speicher-BLOB-Container mit dem Namen des speicherkontos und dem Containernamen zulässige Aufbewahrungstags hinzu.</span><span class="sxs-lookup"><span data-stu-id="9cbed-112">This command adds legal hold tags to a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="9cbed-113">Beispiel 2: Hinzufügen von gültigen Aufbewahrungstags zu einem BLOB-Speichercontainer mit Speicherkonto Objekt und Containernamen</span><span class="sxs-lookup"><span data-stu-id="9cbed-113">Example 2: Add legal hold tags to a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

<span data-ttu-id="9cbed-114">Dieser Befehl fügt einem Speicher-BLOB-Container mit dem Speicherkonto Objekt und dem Containernamen zulässige Aufbewahrungstags hinzu.</span><span class="sxs-lookup"><span data-stu-id="9cbed-114">This command adds legal hold tags to a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="9cbed-115">Beispiel 3: Hinzufügen von gültigen Aufbewahrungstags zu allen BLOB-Speicher Containern in einem Speicherkonto mit Pipeline</span><span class="sxs-lookup"><span data-stu-id="9cbed-115">Example 3: Add legal hold tags to all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

<span data-ttu-id="9cbed-116">Dieser Befehl fügt allen Speicher-BLOB-Containern in einem Speicherkonto mit Pipeline zugelassene Aufbewahrungstags hinzu.</span><span class="sxs-lookup"><span data-stu-id="9cbed-116">This command adds legal hold tags to all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="9cbed-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="9cbed-117">PARAMETERS</span></span>

### <span data-ttu-id="9cbed-118">-Container</span><span class="sxs-lookup"><span data-stu-id="9cbed-118">-Container</span></span>
<span data-ttu-id="9cbed-119">Speichercontainer Objekt</span><span class="sxs-lookup"><span data-stu-id="9cbed-119">Storage container object</span></span>

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

### <span data-ttu-id="9cbed-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cbed-120">-DefaultProfile</span></span>
<span data-ttu-id="9cbed-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9cbed-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cbed-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9cbed-122">-Name</span></span>
<span data-ttu-id="9cbed-123">Container Name</span><span class="sxs-lookup"><span data-stu-id="9cbed-123">Container Name</span></span>

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

### <span data-ttu-id="9cbed-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cbed-124">-ResourceGroupName</span></span>
<span data-ttu-id="9cbed-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9cbed-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="9cbed-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9cbed-126">-StorageAccount</span></span>
<span data-ttu-id="9cbed-127">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="9cbed-127">Storage account object</span></span>

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

### <span data-ttu-id="9cbed-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9cbed-128">-StorageAccountName</span></span>
<span data-ttu-id="9cbed-129">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="9cbed-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="9cbed-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="9cbed-130">-Tag</span></span>
<span data-ttu-id="9cbed-131">Container-LegalHold-Tags</span><span class="sxs-lookup"><span data-stu-id="9cbed-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="9cbed-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9cbed-132">-Confirm</span></span>
<span data-ttu-id="9cbed-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9cbed-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cbed-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cbed-134">-WhatIf</span></span>
<span data-ttu-id="9cbed-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9cbed-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9cbed-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9cbed-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cbed-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cbed-137">CommonParameters</span></span>
<span data-ttu-id="9cbed-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cbed-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cbed-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cbed-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cbed-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9cbed-140">INPUTS</span></span>

### <span data-ttu-id="9cbed-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9cbed-141">System.String</span></span>

### <span data-ttu-id="9cbed-142">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9cbed-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="9cbed-143">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="9cbed-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="9cbed-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9cbed-144">OUTPUTS</span></span>

### <span data-ttu-id="9cbed-145">Microsoft. Azure. Commands. Management. Storage. Models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="9cbed-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="9cbed-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="9cbed-146">NOTES</span></span>

## <span data-ttu-id="9cbed-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9cbed-147">RELATED LINKS</span></span>
