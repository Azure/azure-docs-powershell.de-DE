---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: ''
schema: 2.0.0
ms.openlocfilehash: b273dbec3fda421574c8866a10eda0a8098513ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475782"
---
# <span data-ttu-id="64bb2-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="64bb2-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="64bb2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="64bb2-102">SYNOPSIS</span></span>
<span data-ttu-id="64bb2-103">Legt eine gespeicherte Zugriffsrichtlinie für eine Azure-Speicherwarteschlange fest.</span><span class="sxs-lookup"><span data-stu-id="64bb2-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="64bb2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="64bb2-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64bb2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64bb2-105">DESCRIPTION</span></span>
<span data-ttu-id="64bb2-106">Das Cmdlet " **Set-AzureStorageQueueStoredAccessPolicy** " legt eine gespeicherte Zugriffsrichtlinie für eine Azure-Speicherwarteschlange fest.</span><span class="sxs-lookup"><span data-stu-id="64bb2-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="64bb2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64bb2-107">EXAMPLES</span></span>

### <span data-ttu-id="64bb2-108">Beispiel 1: Festlegen einer gespeicherten Zugriffsrichtlinie in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="64bb2-108">Example 1: Set a stored access policy in the queue</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07"
```

<span data-ttu-id="64bb2-109">Mit diesem Befehl wird eine Zugriffsrichtlinie mit dem Namen Policy07 für die Speicherwarteschlange mit dem Namen myQueue festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64bb2-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="64bb2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="64bb2-110">PARAMETERS</span></span>

### <span data-ttu-id="64bb2-111">-Context</span><span class="sxs-lookup"><span data-stu-id="64bb2-111">-Context</span></span>
<span data-ttu-id="64bb2-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="64bb2-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="64bb2-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="64bb2-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="64bb2-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="64bb2-114">-ExpiryTime</span></span>
<span data-ttu-id="64bb2-115">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="64bb2-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="64bb2-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="64bb2-116">-NoExpiryTime</span></span>
<span data-ttu-id="64bb2-117">Gibt an, dass die Zugriffsrichtlinie kein Ablaufdatum aufweist.</span><span class="sxs-lookup"><span data-stu-id="64bb2-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="64bb2-118">-Nostartzeit</span><span class="sxs-lookup"><span data-stu-id="64bb2-118">-NoStartTime</span></span>
<span data-ttu-id="64bb2-119">Gibt an, dass das Cmdlet die Startzeit auf $NULL festlegt.</span><span class="sxs-lookup"><span data-stu-id="64bb2-119">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="64bb2-120">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="64bb2-120">-Permission</span></span>
<span data-ttu-id="64bb2-121">Gibt die Ebene des öffentlichen Zugriffs auf diese Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="64bb2-121">Specifies the level of public access to this storage queue.</span></span>

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

### <span data-ttu-id="64bb2-122">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="64bb2-122">-Policy</span></span>
<span data-ttu-id="64bb2-123">Gibt eine gespeicherte Zugriffsrichtlinie an, die die Berechtigungen für dieses SAS-Token umfasst.</span><span class="sxs-lookup"><span data-stu-id="64bb2-123">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="64bb2-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="64bb2-124">-Queue</span></span>
<span data-ttu-id="64bb2-125">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="64bb2-125">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="64bb2-126">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="64bb2-126">-StartTime</span></span>
<span data-ttu-id="64bb2-127">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="64bb2-127">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="64bb2-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="64bb2-128">-Confirm</span></span>
<span data-ttu-id="64bb2-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="64bb2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64bb2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64bb2-130">-WhatIf</span></span>
<span data-ttu-id="64bb2-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="64bb2-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64bb2-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="64bb2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64bb2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64bb2-133">CommonParameters</span></span>
<span data-ttu-id="64bb2-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64bb2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64bb2-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64bb2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64bb2-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="64bb2-136">INPUTS</span></span>

## <span data-ttu-id="64bb2-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="64bb2-137">OUTPUTS</span></span>

## <span data-ttu-id="64bb2-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="64bb2-138">NOTES</span></span>

## <span data-ttu-id="64bb2-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="64bb2-139">RELATED LINKS</span></span>

[<span data-ttu-id="64bb2-140">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="64bb2-140">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="64bb2-141">Neu – AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="64bb2-141">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="64bb2-142">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="64bb2-142">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
