---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 69ec2307dfdf8525f892720281079c58c1e1bd55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503341"
---
# <span data-ttu-id="c400b-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c400b-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="c400b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c400b-102">SYNOPSIS</span></span>
<span data-ttu-id="c400b-103">Legt eine gespeicherte Zugriffsrichtlinie für eine Azure-Speicherwarteschlange fest.</span><span class="sxs-lookup"><span data-stu-id="c400b-103">Sets a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c400b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c400b-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c400b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c400b-105">DESCRIPTION</span></span>
<span data-ttu-id="c400b-106">Das Cmdlet " **Set-AzureStorageQueueStoredAccessPolicy** " legt eine gespeicherte Zugriffsrichtlinie für eine Azure-Speicherwarteschlange fest.</span><span class="sxs-lookup"><span data-stu-id="c400b-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="c400b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c400b-107">EXAMPLES</span></span>

### <span data-ttu-id="c400b-108">Beispiel 1: Festlegen einer gespeicherten Zugriffsrichtlinie in der Warteschlange mit der vollständigen Berechtigung</span><span class="sxs-lookup"><span data-stu-id="c400b-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="c400b-109">Mit diesem Befehl wird eine Zugriffsrichtlinie mit dem Namen Policy07 für die Speicherwarteschlange mit dem Namen myQueue festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c400b-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="c400b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c400b-110">PARAMETERS</span></span>

### <span data-ttu-id="c400b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c400b-111">-Context</span></span>
<span data-ttu-id="c400b-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="c400b-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c400b-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c400b-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c400b-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c400b-114">-ExpiryTime</span></span>
<span data-ttu-id="c400b-115">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="c400b-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c400b-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c400b-116">-NoExpiryTime</span></span>
<span data-ttu-id="c400b-117">Gibt an, dass die Zugriffsrichtlinie kein Ablaufdatum aufweist.</span><span class="sxs-lookup"><span data-stu-id="c400b-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="c400b-118">-Nostartzeit</span><span class="sxs-lookup"><span data-stu-id="c400b-118">-NoStartTime</span></span>
<span data-ttu-id="c400b-119">Gibt an, dass das Cmdlet die Startzeit auf $NULL festlegt.</span><span class="sxs-lookup"><span data-stu-id="c400b-119">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="c400b-120">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="c400b-120">-Permission</span></span>
<span data-ttu-id="c400b-121">Gibt Berechtigungen in der gespeicherten Zugriffsrichtlinie an, um auf die Speicherwarteschlange zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c400b-121">Specifies permissions in the stored access policy to access the storage queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c400b-122">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="c400b-122">-Policy</span></span>
<span data-ttu-id="c400b-123">Gibt den Namen für die gespeicherte Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="c400b-123">Specifies the name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c400b-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="c400b-124">-Queue</span></span>
<span data-ttu-id="c400b-125">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="c400b-125">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c400b-126">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="c400b-126">-StartTime</span></span>
<span data-ttu-id="c400b-127">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="c400b-127">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c400b-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c400b-128">-Confirm</span></span>
<span data-ttu-id="c400b-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c400b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c400b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c400b-130">-WhatIf</span></span>
<span data-ttu-id="c400b-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c400b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c400b-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c400b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c400b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c400b-133">CommonParameters</span></span>
<span data-ttu-id="c400b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c400b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c400b-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c400b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c400b-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c400b-136">INPUTS</span></span>

### <span data-ttu-id="c400b-137">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c400b-137">IStorageContext</span></span>

<span data-ttu-id="c400b-138">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c400b-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="c400b-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c400b-139">String</span></span>

<span data-ttu-id="c400b-140">Der Parameter "Queue" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c400b-140">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="c400b-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c400b-141">OUTPUTS</span></span>

### <span data-ttu-id="c400b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c400b-142">System.String</span></span>

## <span data-ttu-id="c400b-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="c400b-143">NOTES</span></span>

## <span data-ttu-id="c400b-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c400b-144">RELATED LINKS</span></span>

[<span data-ttu-id="c400b-145">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c400b-145">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="c400b-146">Neu – AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c400b-146">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="c400b-147">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c400b-147">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
