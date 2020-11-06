---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: f4dfc77be9006229e2919dd1a4e0cdb1dd8c548e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499318"
---
# <span data-ttu-id="5f1fb-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5f1fb-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="5f1fb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f1fb-102">SYNOPSIS</span></span>
<span data-ttu-id="5f1fb-103">Legt die Richtlinie für den gespeicherten Zugriff für eine Azure-Speichertabelle fest.</span><span class="sxs-lookup"><span data-stu-id="5f1fb-103">Sets the stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f1fb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f1fb-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f1fb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f1fb-105">DESCRIPTION</span></span>
<span data-ttu-id="5f1fb-106">Mit dem Cmdlet " **festlegen-AzureStorageTableStoredAccessPolicy** " wird die Richtlinie für den gespeicherten Zugriff für eine Azure-Speichertabelle definiert.</span><span class="sxs-lookup"><span data-stu-id="5f1fb-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="5f1fb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f1fb-107">EXAMPLES</span></span>

### <span data-ttu-id="5f1fb-108">Beispiel 1: Festlegen einer gespeicherten Zugriffsrichtlinie in einer Tabelle mit der vollständigen Berechtigung</span><span class="sxs-lookup"><span data-stu-id="5f1fb-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="5f1fb-109">Mit diesem Befehl wird eine Zugriffsrichtlinie mit dem Namen Policy08 für die Speichertabelle "MyTable" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5f1fb-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="5f1fb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f1fb-110">PARAMETERS</span></span>

### <span data-ttu-id="5f1fb-111">-Context</span><span class="sxs-lookup"><span data-stu-id="5f1fb-111">-Context</span></span>
<span data-ttu-id="5f1fb-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="5f1fb-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5f1fb-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5f1fb-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5f1fb-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5f1fb-114">-ExpiryTime</span></span>
<span data-ttu-id="5f1fb-115">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie abläuft.</span><span class="sxs-lookup"><span data-stu-id="5f1fb-115">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="5f1fb-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5f1fb-116">-NoExpiryTime</span></span>
<span data-ttu-id="5f1fb-117">Gibt an, dass die Zugriffsrichtlinie kein Ablaufdatum aufweist.</span><span class="sxs-lookup"><span data-stu-id="5f1fb-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="5f1fb-118">-Nostartzeit</span><span class="sxs-lookup"><span data-stu-id="5f1fb-118">-NoStartTime</span></span>
<span data-ttu-id="5f1fb-119">Gibt an, dass die Startzeit auf $Null festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="5f1fb-119">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="5f1fb-120">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="5f1fb-120">-Permission</span></span>
<span data-ttu-id="5f1fb-121">Gibt Berechtigungen in der gespeicherten Zugriffsrichtlinie an, um auf die Speichertabelle zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="5f1fb-121">Specifies permissions in the stored access policy to access the storage table.</span></span>

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

### <span data-ttu-id="5f1fb-122">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="5f1fb-122">-Policy</span></span>
<span data-ttu-id="5f1fb-123">Gibt den Namen für die gespeicherte Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="5f1fb-123">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="5f1fb-124">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="5f1fb-124">-StartTime</span></span>
<span data-ttu-id="5f1fb-125">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="5f1fb-125">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="5f1fb-126">-Tabelle</span><span class="sxs-lookup"><span data-stu-id="5f1fb-126">-Table</span></span>
<span data-ttu-id="5f1fb-127">Gibt den Namen der Azure-Speichertabelle an.</span><span class="sxs-lookup"><span data-stu-id="5f1fb-127">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="5f1fb-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5f1fb-128">-Confirm</span></span>
<span data-ttu-id="5f1fb-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5f1fb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f1fb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f1fb-130">-WhatIf</span></span>
<span data-ttu-id="5f1fb-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f1fb-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f1fb-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f1fb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f1fb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f1fb-133">CommonParameters</span></span>
<span data-ttu-id="5f1fb-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f1fb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f1fb-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f1fb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f1fb-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f1fb-136">INPUTS</span></span>

### <span data-ttu-id="5f1fb-137">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5f1fb-137">IStorageContext</span></span>

<span data-ttu-id="5f1fb-138">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5f1fb-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="5f1fb-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5f1fb-139">String</span></span>

<span data-ttu-id="5f1fb-140">Der Parameter "Tabelle" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5f1fb-140">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5f1fb-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f1fb-141">OUTPUTS</span></span>

### <span data-ttu-id="5f1fb-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5f1fb-142">System.String</span></span>

## <span data-ttu-id="5f1fb-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f1fb-143">NOTES</span></span>

## <span data-ttu-id="5f1fb-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f1fb-144">RELATED LINKS</span></span>

[<span data-ttu-id="5f1fb-145">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5f1fb-145">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="5f1fb-146">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5f1fb-146">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="5f1fb-147">Neu – AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5f1fb-147">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="5f1fb-148">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5f1fb-148">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)
