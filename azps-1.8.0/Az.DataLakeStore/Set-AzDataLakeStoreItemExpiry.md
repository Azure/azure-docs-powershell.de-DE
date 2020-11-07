---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
ms.openlocfilehash: 074e6224c7a5b1ea1e8039901b75d223581495d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661256"
---
# <span data-ttu-id="6b49b-101">Set-AzDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="6b49b-101">Set-AzDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="6b49b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6b49b-102">SYNOPSIS</span></span>
<span data-ttu-id="6b49b-103">Legt die Ablaufzeit für eine Datei in einem Azure Data Lake Store-Konto fest oder entfernt Sie.</span><span class="sxs-lookup"><span data-stu-id="6b49b-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="6b49b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b49b-104">SYNTAX</span></span>

### <span data-ttu-id="6b49b-105">SetAbsoluteNeverExpireExpiry (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b49b-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b49b-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="6b49b-106">SetRelativeExpiry</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b49b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b49b-107">DESCRIPTION</span></span>
<span data-ttu-id="6b49b-108">Das Cmdlet " **Set-AzDataLakeStoreItemExpiry** " legt die Ablaufzeit für eine Datei in einem Azure Data Lake Store-Konto fest oder entfernt Sie.</span><span class="sxs-lookup"><span data-stu-id="6b49b-108">The **Set-AzDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="6b49b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b49b-109">EXAMPLES</span></span>

### <span data-ttu-id="6b49b-110">Beispiel 1: Einrichten der Ablaufzeit für eine Datei</span><span class="sxs-lookup"><span data-stu-id="6b49b-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="6b49b-111">Legt das Ablaufdatum für die Datei myfile.txt in Konto ContosoADL auf zwei Stunden fest.</span><span class="sxs-lookup"><span data-stu-id="6b49b-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="6b49b-112">Dies führt dazu, dass die Datei in zwei Stunden abläuft (für DELETE markiert ist).</span><span class="sxs-lookup"><span data-stu-id="6b49b-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="6b49b-113">Beispiel 2: Entfernen des Ablaufs für eine Datei</span><span class="sxs-lookup"><span data-stu-id="6b49b-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="6b49b-114">Entfernt alle Ablaufdaten, die zuvor für die Datei "myfile.txt" im Konto "ContosoADL" festgesetzt wurden.</span><span class="sxs-lookup"><span data-stu-id="6b49b-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="6b49b-115">Dies bedeutet, dass die Datei nicht automatisch abläuft (für DELETE markiert ist) und manuell gelöscht oder wieder ablaufen muss.</span><span class="sxs-lookup"><span data-stu-id="6b49b-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

### <span data-ttu-id="6b49b-116">Beispiel 3: Legen Sie die Ablaufzeit für eine Datei relativ zu jetzt</span><span class="sxs-lookup"><span data-stu-id="6b49b-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="6b49b-117">Der erste Befehl legt die Ablaufzeit der Datei/myfile.txt 240 Sekunden relativ zur aktuellen Uhrzeit auf dem Server fest.</span><span class="sxs-lookup"><span data-stu-id="6b49b-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>
<span data-ttu-id="6b49b-118">Der zweite Befehl legt die Ablaufzeit für die Datei/myfile.txt 240 Sekunden relativ zum Erstellungszeitpunkt auf dem Server fest.</span><span class="sxs-lookup"><span data-stu-id="6b49b-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="6b49b-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b49b-119">PARAMETERS</span></span>

### <span data-ttu-id="6b49b-120">-Konto</span><span class="sxs-lookup"><span data-stu-id="6b49b-120">-Account</span></span>
<span data-ttu-id="6b49b-121">Gibt den Namen des Daten Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="6b49b-121">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b49b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b49b-122">-DefaultProfile</span></span>
<span data-ttu-id="6b49b-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6b49b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b49b-124">-Ablauf</span><span class="sxs-lookup"><span data-stu-id="6b49b-124">-Expiration</span></span>
<span data-ttu-id="6b49b-125">Die absolute Ablaufzeit für die angegebene Datei.</span><span class="sxs-lookup"><span data-stu-id="6b49b-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="6b49b-126">Wenn kein Wert oder auf MaxValue gesetzt wird, läuft die Datei nie ab.</span><span class="sxs-lookup"><span data-stu-id="6b49b-126">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: SetAbsoluteNeverExpireExpiry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b49b-127">-Path</span><span class="sxs-lookup"><span data-stu-id="6b49b-127">-Path</span></span>
<span data-ttu-id="6b49b-128">Gibt den Daten See-Speicherpfad für das Dateielement an, für das das Ablaufdatum festgelegt oder entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b49b-128">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b49b-129">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="6b49b-129">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="6b49b-130">Relative Ablauf Optionen.</span><span class="sxs-lookup"><span data-stu-id="6b49b-130">Relative expiry options.</span></span> <span data-ttu-id="6b49b-131">RelativeToNow oder RelativeToCreationDate sind aktuelle Optionen</span><span class="sxs-lookup"><span data-stu-id="6b49b-131">RelativeToNow or RelativeToCreationDate are current options</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions
Parameter Sets: SetRelativeExpiry
Aliases:
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b49b-132">-Relativzeit</span><span class="sxs-lookup"><span data-stu-id="6b49b-132">-RelativeTime</span></span>
<span data-ttu-id="6b49b-133">Relative Zeit in Millisekunden in Bezug auf "jetzt" oder "Erstellungszeit"</span><span class="sxs-lookup"><span data-stu-id="6b49b-133">The relative time in milliseconds with respect to now or creation time</span></span>

```yaml
Type: System.Int64
Parameter Sets: SetRelativeExpiry
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b49b-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6b49b-134">-Confirm</span></span>
<span data-ttu-id="6b49b-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6b49b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b49b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b49b-136">-WhatIf</span></span>
<span data-ttu-id="6b49b-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6b49b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b49b-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b49b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b49b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b49b-139">CommonParameters</span></span>
<span data-ttu-id="6b49b-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b49b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b49b-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b49b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b49b-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6b49b-142">INPUTS</span></span>

### <span data-ttu-id="6b49b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="6b49b-143">System.String</span></span>

### <span data-ttu-id="6b49b-144">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="6b49b-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="6b49b-145">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6b49b-145">System.DateTimeOffset</span></span>

### <span data-ttu-id="6b49b-146">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + PathRelativeExpiryOptions</span><span class="sxs-lookup"><span data-stu-id="6b49b-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span></span>

### <span data-ttu-id="6b49b-147">System. Int64</span><span class="sxs-lookup"><span data-stu-id="6b49b-147">System.Int64</span></span>

## <span data-ttu-id="6b49b-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6b49b-148">OUTPUTS</span></span>

### <span data-ttu-id="6b49b-149">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6b49b-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="6b49b-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="6b49b-150">NOTES</span></span>
<span data-ttu-id="6b49b-151">Alias: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="6b49b-151">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="6b49b-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6b49b-152">RELATED LINKS</span></span>

[<span data-ttu-id="6b49b-153">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6b49b-153">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

