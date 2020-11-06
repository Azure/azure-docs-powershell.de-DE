---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54770fd564addf30e7c4ed058776857b823903e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475566"
---
# <span data-ttu-id="13581-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="13581-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="13581-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="13581-102">SYNOPSIS</span></span>
<span data-ttu-id="13581-103">Entfernt eine Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="13581-103">Removes a storage queue.</span></span>

## <span data-ttu-id="13581-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="13581-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13581-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13581-105">DESCRIPTION</span></span>
<span data-ttu-id="13581-106">Das Cmdlet **Remove-AzureStorageQueue** entfernt eine Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="13581-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="13581-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="13581-107">EXAMPLES</span></span>

### <span data-ttu-id="13581-108">Beispiel 1: Entfernen einer Speicherwarteschlange nach Namen</span><span class="sxs-lookup"><span data-stu-id="13581-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="13581-109">Dieser Befehl entfernt eine Warteschlange mit dem Namen ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="13581-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="13581-110">Beispiel 2: Entfernen mehrerer Speicher Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="13581-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="13581-111">Mit diesem Befehl werden alle Warteschlangen mit Namen entfernt, die mit Contoso beginnen.</span><span class="sxs-lookup"><span data-stu-id="13581-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="13581-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="13581-112">PARAMETERS</span></span>

### <span data-ttu-id="13581-113">-Context</span><span class="sxs-lookup"><span data-stu-id="13581-113">-Context</span></span>
<span data-ttu-id="13581-114">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="13581-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="13581-115">Zum Abrufen des Speicher Kontexts das New-AzureStorageContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13581-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="13581-116">-Force</span><span class="sxs-lookup"><span data-stu-id="13581-116">-Force</span></span>
<span data-ttu-id="13581-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="13581-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="13581-118">-Name</span><span class="sxs-lookup"><span data-stu-id="13581-118">-Name</span></span>
<span data-ttu-id="13581-119">Gibt den Namen der zu entfernenden Warteschlange an.</span><span class="sxs-lookup"><span data-stu-id="13581-119">Specifies the name of the queue to remove.</span></span>

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

### <span data-ttu-id="13581-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13581-120">-PassThru</span></span>
<span data-ttu-id="13581-121">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="13581-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="13581-122">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="13581-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="13581-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="13581-123">-Confirm</span></span>
<span data-ttu-id="13581-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="13581-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13581-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13581-125">-WhatIf</span></span>
<span data-ttu-id="13581-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="13581-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13581-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="13581-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13581-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13581-128">CommonParameters</span></span>
<span data-ttu-id="13581-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13581-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13581-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13581-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13581-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="13581-131">INPUTS</span></span>

## <span data-ttu-id="13581-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="13581-132">OUTPUTS</span></span>

## <span data-ttu-id="13581-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="13581-133">NOTES</span></span>

## <span data-ttu-id="13581-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="13581-134">RELATED LINKS</span></span>

[<span data-ttu-id="13581-135">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="13581-135">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="13581-136">Neu – AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="13581-136">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)
