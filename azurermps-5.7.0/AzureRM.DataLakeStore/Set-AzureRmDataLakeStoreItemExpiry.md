---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: 6908bc4d474d0dbe9df045332f3820b5f7536dac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500622"
---
# <span data-ttu-id="37ab8-101">Set-AzureRmDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="37ab8-101">Set-AzureRmDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="37ab8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37ab8-102">SYNOPSIS</span></span>
<span data-ttu-id="37ab8-103">Legt die Ablaufzeit für eine Datei in einem Azure Data Lake Store-Konto fest oder entfernt Sie.</span><span class="sxs-lookup"><span data-stu-id="37ab8-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37ab8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37ab8-104">SYNTAX</span></span>

### <span data-ttu-id="37ab8-105">SetAbsoluteNeverExpireExpiry (Standard)</span><span class="sxs-lookup"><span data-stu-id="37ab8-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37ab8-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="37ab8-106">SetRelativeExpiry</span></span>
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-RelativeFileExpiryOption] <PathRelativeExpiryOptions>] [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37ab8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37ab8-107">DESCRIPTION</span></span>
<span data-ttu-id="37ab8-108">Das Cmdlet " **Set-AzureRmDataLakeStoreItemExpiry** " legt die Ablaufzeit für eine Datei in einem Azure Data Lake Store-Konto fest oder entfernt Sie.</span><span class="sxs-lookup"><span data-stu-id="37ab8-108">The **Set-AzureRmDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="37ab8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37ab8-109">EXAMPLES</span></span>

### <span data-ttu-id="37ab8-110">Beispiel 1: Einrichten der Ablaufzeit für eine Datei</span><span class="sxs-lookup"><span data-stu-id="37ab8-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="37ab8-111">Legt das Ablaufdatum für die Datei myfile.txt in Konto ContosoADL auf zwei Stunden fest.</span><span class="sxs-lookup"><span data-stu-id="37ab8-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="37ab8-112">Dies führt dazu, dass die Datei in zwei Stunden abläuft (für DELETE markiert ist).</span><span class="sxs-lookup"><span data-stu-id="37ab8-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="37ab8-113">Beispiel 2: Entfernen des Ablaufs für eine Datei</span><span class="sxs-lookup"><span data-stu-id="37ab8-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="37ab8-114">Entfernt alle Ablaufdaten, die zuvor für die Datei "myfile.txt" im Konto "ContosoADL" festgesetzt wurden.</span><span class="sxs-lookup"><span data-stu-id="37ab8-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="37ab8-115">Dies bedeutet, dass die Datei nicht automatisch abläuft (für DELETE markiert ist) und manuell gelöscht oder wieder ablaufen muss.</span><span class="sxs-lookup"><span data-stu-id="37ab8-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>


### <span data-ttu-id="37ab8-116">Beispiel 3: Legen Sie die Ablaufzeit für eine Datei relativ zu jetzt</span><span class="sxs-lookup"><span data-stu-id="37ab8-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="37ab8-117">Der erste Befehl legt die Ablaufzeit der Datei/myfile.txt 240 Sekunden relativ zur aktuellen Uhrzeit auf dem Server fest.</span><span class="sxs-lookup"><span data-stu-id="37ab8-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>

<span data-ttu-id="37ab8-118">Der zweite Befehl legt die Ablaufzeit für die Datei/myfile.txt 240 Sekunden relativ zum Erstellungszeitpunkt auf dem Server fest.</span><span class="sxs-lookup"><span data-stu-id="37ab8-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="37ab8-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="37ab8-119">PARAMETERS</span></span>

### <span data-ttu-id="37ab8-120">-Konto</span><span class="sxs-lookup"><span data-stu-id="37ab8-120">-Account</span></span>
<span data-ttu-id="37ab8-121">Gibt den Namen des Daten Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="37ab8-121">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ab8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37ab8-122">-DefaultProfile</span></span>
<span data-ttu-id="37ab8-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="37ab8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37ab8-124">-Ablauf</span><span class="sxs-lookup"><span data-stu-id="37ab8-124">-Expiration</span></span>
<span data-ttu-id="37ab8-125">Die absolute Ablaufzeit für die angegebene Datei.</span><span class="sxs-lookup"><span data-stu-id="37ab8-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="37ab8-126">Wenn kein Wert oder auf MaxValue gesetzt wird, läuft die Datei nie ab.</span><span class="sxs-lookup"><span data-stu-id="37ab8-126">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: Set expiry as Absolute or NeverExpire
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ab8-127">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="37ab8-127">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="37ab8-128">Relative Ablauf Optionen.</span><span class="sxs-lookup"><span data-stu-id="37ab8-128">Relative expiry options.</span></span> <span data-ttu-id="37ab8-129">RelativeToNow oder RelativeToCreationDate sind aktuelle Optionen</span><span class="sxs-lookup"><span data-stu-id="37ab8-129">RelativeToNow or RelativeToCreationDate are current options</span></span>
```yaml
Type: PathRelativeExpiryOptions
Parameter Sets: Set expiry as relative to creation or now
Aliases: 
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ab8-130">-Path</span><span class="sxs-lookup"><span data-stu-id="37ab8-130">-Path</span></span>
<span data-ttu-id="37ab8-131">Gibt den Daten See-Speicherpfad für das Dateielement an, für das das Ablaufdatum festgelegt oder entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="37ab8-131">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ab8-132">-Relativzeit</span><span class="sxs-lookup"><span data-stu-id="37ab8-132">-RelativeTime</span></span>
<span data-ttu-id="37ab8-133">Relative Zeit in Millisekunden in Bezug auf "jetzt" oder "Erstellungszeit"</span><span class="sxs-lookup"><span data-stu-id="37ab8-133">The relative time in milliseconds with respect to now or creation time</span></span>
```yaml
Type: Int64
Parameter Sets: Set expiry as relative to creation or now
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ab8-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="37ab8-134">-Confirm</span></span>
<span data-ttu-id="37ab8-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="37ab8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37ab8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37ab8-136">-WhatIf</span></span>
<span data-ttu-id="37ab8-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37ab8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37ab8-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37ab8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37ab8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37ab8-139">CommonParameters</span></span>
<span data-ttu-id="37ab8-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37ab8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37ab8-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37ab8-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37ab8-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37ab8-142">INPUTS</span></span>

### <span data-ttu-id="37ab8-143">Keine</span><span class="sxs-lookup"><span data-stu-id="37ab8-143">None</span></span>
<span data-ttu-id="37ab8-144">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="37ab8-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="37ab8-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37ab8-145">OUTPUTS</span></span>

### <span data-ttu-id="37ab8-146">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="37ab8-146">DataLakeStoreItem</span></span>
<span data-ttu-id="37ab8-147">Die aktualisierte Datei mit einer neuen Ablaufzeit.</span><span class="sxs-lookup"><span data-stu-id="37ab8-147">The updated file with a new expiration time.</span></span>

## <span data-ttu-id="37ab8-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="37ab8-148">NOTES</span></span>
<span data-ttu-id="37ab8-149">Alias: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="37ab8-149">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="37ab8-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37ab8-150">RELATED LINKS</span></span>

[<span data-ttu-id="37ab8-151">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="37ab8-151">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

