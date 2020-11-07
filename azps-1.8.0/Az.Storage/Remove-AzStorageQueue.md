---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
ms.openlocfilehash: 2afb39aafacef354c4e50aad1ce0a4824622c9c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658773"
---
# <span data-ttu-id="244d3-101">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="244d3-101">Remove-AzStorageQueue</span></span>

## <span data-ttu-id="244d3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="244d3-102">SYNOPSIS</span></span>
<span data-ttu-id="244d3-103">Entfernt eine Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="244d3-103">Removes a storage queue.</span></span>

## <span data-ttu-id="244d3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="244d3-104">SYNTAX</span></span>

```
Remove-AzStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="244d3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="244d3-105">DESCRIPTION</span></span>
<span data-ttu-id="244d3-106">Das Cmdlet **Remove-AzStorageQueue** entfernt eine Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="244d3-106">The **Remove-AzStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="244d3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="244d3-107">EXAMPLES</span></span>

### <span data-ttu-id="244d3-108">Beispiel 1: Entfernen einer Speicherwarteschlange nach Namen</span><span class="sxs-lookup"><span data-stu-id="244d3-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzStorageQueue "ContosoQueue01"
```

<span data-ttu-id="244d3-109">Dieser Befehl entfernt eine Warteschlange mit dem Namen ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="244d3-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="244d3-110">Beispiel 2: Entfernen mehrerer Speicher Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="244d3-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzStorageQueue "Contoso*" | Remove-AzStorageQueue
```

<span data-ttu-id="244d3-111">Mit diesem Befehl werden alle Warteschlangen mit Namen entfernt, die mit Contoso beginnen.</span><span class="sxs-lookup"><span data-stu-id="244d3-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="244d3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="244d3-112">PARAMETERS</span></span>

### <span data-ttu-id="244d3-113">-Context</span><span class="sxs-lookup"><span data-stu-id="244d3-113">-Context</span></span>
<span data-ttu-id="244d3-114">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="244d3-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="244d3-115">Zum Abrufen des Speicher Kontexts das New-AzStorageContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="244d3-115">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="244d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="244d3-116">-DefaultProfile</span></span>
<span data-ttu-id="244d3-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="244d3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="244d3-118">-Force</span><span class="sxs-lookup"><span data-stu-id="244d3-118">-Force</span></span>
<span data-ttu-id="244d3-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="244d3-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="244d3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="244d3-120">-Name</span></span>
<span data-ttu-id="244d3-121">Gibt den Namen der zu entfernenden Warteschlange an.</span><span class="sxs-lookup"><span data-stu-id="244d3-121">Specifies the name of the queue to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="244d3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="244d3-122">-PassThru</span></span>
<span data-ttu-id="244d3-123">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="244d3-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="244d3-124">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="244d3-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="244d3-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="244d3-125">-Confirm</span></span>
<span data-ttu-id="244d3-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="244d3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="244d3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="244d3-127">-WhatIf</span></span>
<span data-ttu-id="244d3-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="244d3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="244d3-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="244d3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="244d3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="244d3-130">CommonParameters</span></span>
<span data-ttu-id="244d3-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="244d3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="244d3-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="244d3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="244d3-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="244d3-133">INPUTS</span></span>

### <span data-ttu-id="244d3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="244d3-134">System.String</span></span>

### <span data-ttu-id="244d3-135">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="244d3-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="244d3-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="244d3-136">OUTPUTS</span></span>

### <span data-ttu-id="244d3-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="244d3-137">System.Boolean</span></span>

## <span data-ttu-id="244d3-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="244d3-138">NOTES</span></span>

## <span data-ttu-id="244d3-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="244d3-139">RELATED LINKS</span></span>

[<span data-ttu-id="244d3-140">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="244d3-140">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="244d3-141">Neu – AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="244d3-141">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)
