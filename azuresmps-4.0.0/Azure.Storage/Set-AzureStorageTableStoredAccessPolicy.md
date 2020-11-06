---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: ''
schema: 2.0.0
ms.openlocfilehash: d517ca49f0be3b6add58d151b3b2f79dad17611c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475773"
---
# <span data-ttu-id="4cb51-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4cb51-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="4cb51-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4cb51-102">SYNOPSIS</span></span>
<span data-ttu-id="4cb51-103">Legt die Richtlinie für den gespeicherten Zugriff für eine Azure-Speichertabelle fest.</span><span class="sxs-lookup"><span data-stu-id="4cb51-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="4cb51-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cb51-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cb51-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4cb51-105">DESCRIPTION</span></span>
<span data-ttu-id="4cb51-106">Mit dem Cmdlet " **festlegen-AzureStorageTableStoredAccessPolicy** " wird die Richtlinie für den gespeicherten Zugriff für eine Azure-Speichertabelle definiert.</span><span class="sxs-lookup"><span data-stu-id="4cb51-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="4cb51-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4cb51-107">EXAMPLES</span></span>

### <span data-ttu-id="4cb51-108">Beispiel 1: Festlegen einer gespeicherten Zugriffsrichtlinie in einer Tabelle mit der vollständigen Berechtigung</span><span class="sxs-lookup"><span data-stu-id="4cb51-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08"
```

<span data-ttu-id="4cb51-109">Mit diesem Befehl wird eine Zugriffsrichtlinie mit dem Namen Policy08 für die Speichertabelle "MyTable" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4cb51-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="4cb51-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cb51-110">PARAMETERS</span></span>

### <span data-ttu-id="4cb51-111">-Context</span><span class="sxs-lookup"><span data-stu-id="4cb51-111">-Context</span></span>
<span data-ttu-id="4cb51-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="4cb51-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4cb51-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4cb51-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4cb51-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4cb51-114">-ExpiryTime</span></span>
<span data-ttu-id="4cb51-115">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie abläuft.</span><span class="sxs-lookup"><span data-stu-id="4cb51-115">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="4cb51-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4cb51-116">-NoExpiryTime</span></span>
<span data-ttu-id="4cb51-117">Gibt an, dass die Zugriffsrichtlinie kein Ablaufdatum aufweist.</span><span class="sxs-lookup"><span data-stu-id="4cb51-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="4cb51-118">-Nostartzeit</span><span class="sxs-lookup"><span data-stu-id="4cb51-118">-NoStartTime</span></span>
<span data-ttu-id="4cb51-119">Gibt an, dass die Startzeit auf $Null festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="4cb51-119">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="4cb51-120">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="4cb51-120">-Permission</span></span>
<span data-ttu-id="4cb51-121">Gibt die Ebene des öffentlichen Zugriffs auf diese Speichertabelle an.</span><span class="sxs-lookup"><span data-stu-id="4cb51-121">Specifies the level of public access to this storage table.</span></span>

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

### <span data-ttu-id="4cb51-122">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="4cb51-122">-Policy</span></span>
<span data-ttu-id="4cb51-123">Gibt eine gespeicherte Zugriffsrichtlinie an, die die Berechtigungen für dieses SAS-Token umfasst.</span><span class="sxs-lookup"><span data-stu-id="4cb51-123">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="4cb51-124">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="4cb51-124">-StartTime</span></span>
<span data-ttu-id="4cb51-125">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="4cb51-125">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="4cb51-126">-Tabelle</span><span class="sxs-lookup"><span data-stu-id="4cb51-126">-Table</span></span>
<span data-ttu-id="4cb51-127">Gibt den Namen der Azure-Speichertabelle an.</span><span class="sxs-lookup"><span data-stu-id="4cb51-127">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="4cb51-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4cb51-128">-Confirm</span></span>
<span data-ttu-id="4cb51-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4cb51-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cb51-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cb51-130">-WhatIf</span></span>
<span data-ttu-id="4cb51-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4cb51-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4cb51-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4cb51-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cb51-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cb51-133">CommonParameters</span></span>
<span data-ttu-id="4cb51-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cb51-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cb51-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cb51-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cb51-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4cb51-136">INPUTS</span></span>

## <span data-ttu-id="4cb51-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4cb51-137">OUTPUTS</span></span>

## <span data-ttu-id="4cb51-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="4cb51-138">NOTES</span></span>

## <span data-ttu-id="4cb51-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4cb51-139">RELATED LINKS</span></span>

[<span data-ttu-id="4cb51-140">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4cb51-140">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="4cb51-141">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="4cb51-141">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="4cb51-142">Neu – AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4cb51-142">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="4cb51-143">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4cb51-143">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)
