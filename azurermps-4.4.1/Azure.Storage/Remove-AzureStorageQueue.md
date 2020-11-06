---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 51ea3111b5010b0e29f7bfd69ed5a8e66e596113
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480026"
---
# <span data-ttu-id="17a48-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="17a48-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="17a48-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="17a48-102">SYNOPSIS</span></span>
<span data-ttu-id="17a48-103">Entfernt eine Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="17a48-103">Removes a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17a48-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="17a48-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17a48-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17a48-105">DESCRIPTION</span></span>
<span data-ttu-id="17a48-106">Das Cmdlet **Remove-AzureStorageQueue** entfernt eine Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="17a48-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="17a48-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="17a48-107">EXAMPLES</span></span>

### <span data-ttu-id="17a48-108">Beispiel 1: Entfernen einer Speicherwarteschlange nach Namen</span><span class="sxs-lookup"><span data-stu-id="17a48-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="17a48-109">Dieser Befehl entfernt eine Warteschlange mit dem Namen ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="17a48-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="17a48-110">Beispiel 2: Entfernen mehrerer Speicher Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="17a48-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="17a48-111">Mit diesem Befehl werden alle Warteschlangen mit Namen entfernt, die mit Contoso beginnen.</span><span class="sxs-lookup"><span data-stu-id="17a48-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="17a48-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="17a48-112">PARAMETERS</span></span>

### <span data-ttu-id="17a48-113">-Context</span><span class="sxs-lookup"><span data-stu-id="17a48-113">-Context</span></span>
<span data-ttu-id="17a48-114">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="17a48-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="17a48-115">Zum Abrufen des Speicher Kontexts das New-AzureStorageContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17a48-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17a48-116">-Force</span><span class="sxs-lookup"><span data-stu-id="17a48-116">-Force</span></span>
<span data-ttu-id="17a48-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="17a48-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a48-118">-Name</span><span class="sxs-lookup"><span data-stu-id="17a48-118">-Name</span></span>
<span data-ttu-id="17a48-119">Gibt den Namen der zu entfernenden Warteschlange an.</span><span class="sxs-lookup"><span data-stu-id="17a48-119">Specifies the name of the queue to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17a48-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17a48-120">-PassThru</span></span>
<span data-ttu-id="17a48-121">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="17a48-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="17a48-122">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="17a48-122">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a48-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="17a48-123">-Confirm</span></span>
<span data-ttu-id="17a48-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="17a48-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a48-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17a48-125">-WhatIf</span></span>
<span data-ttu-id="17a48-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="17a48-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17a48-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="17a48-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a48-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17a48-128">CommonParameters</span></span>
<span data-ttu-id="17a48-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17a48-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17a48-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17a48-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17a48-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="17a48-131">INPUTS</span></span>

### <span data-ttu-id="17a48-132">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="17a48-132">IStorageContext</span></span>

<span data-ttu-id="17a48-133">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="17a48-133">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="17a48-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="17a48-134">String</span></span>

<span data-ttu-id="17a48-135">Der Parameter "Name" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="17a48-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="17a48-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="17a48-136">OUTPUTS</span></span>

### <span data-ttu-id="17a48-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="17a48-137">System.Boolean</span></span>

## <span data-ttu-id="17a48-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="17a48-138">NOTES</span></span>

## <span data-ttu-id="17a48-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="17a48-139">RELATED LINKS</span></span>

[<span data-ttu-id="17a48-140">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="17a48-140">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="17a48-141">Neu – AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="17a48-141">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)
