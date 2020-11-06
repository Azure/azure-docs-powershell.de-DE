---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: f71c26e69f9f297a23d4e6902ca6aaac6b135c42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505957"
---
# <span data-ttu-id="77052-101">Set-AzureRmDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="77052-101">Set-AzureRmDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="77052-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="77052-102">SYNOPSIS</span></span>
<span data-ttu-id="77052-103">Legt die Ablaufzeit für eine Datei in einem Azure Data Lake Store-Konto fest oder entfernt Sie.</span><span class="sxs-lookup"><span data-stu-id="77052-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77052-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="77052-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77052-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="77052-105">DESCRIPTION</span></span>
<span data-ttu-id="77052-106">Das Cmdlet " **Set-AzureRmDataLakeStoreItemExpiry** " legt die Ablaufzeit für eine Datei in einem Azure Data Lake Store-Konto fest oder entfernt Sie.</span><span class="sxs-lookup"><span data-stu-id="77052-106">The **Set-AzureRmDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="77052-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="77052-107">EXAMPLES</span></span>

### <span data-ttu-id="77052-108">Beispiel 1: Einrichten der Ablaufzeit für eine Datei</span><span class="sxs-lookup"><span data-stu-id="77052-108">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="77052-109">Legt das Ablaufdatum für die Datei myfile.txt in Konto ContosoADL auf zwei Stunden fest.</span><span class="sxs-lookup"><span data-stu-id="77052-109">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="77052-110">Dies führt dazu, dass die Datei in zwei Stunden abläuft (für DELETE markiert ist).</span><span class="sxs-lookup"><span data-stu-id="77052-110">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="77052-111">Beispiel 2: Entfernen des Ablaufs für eine Datei</span><span class="sxs-lookup"><span data-stu-id="77052-111">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="77052-112">Entfernt alle Ablaufdaten, die zuvor für die Datei "myfile.txt" im Konto "ContosoADL" festgesetzt wurden.</span><span class="sxs-lookup"><span data-stu-id="77052-112">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="77052-113">Dies bedeutet, dass die Datei nicht automatisch abläuft (für DELETE markiert ist) und manuell gelöscht oder wieder ablaufen muss.</span><span class="sxs-lookup"><span data-stu-id="77052-113">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

## <span data-ttu-id="77052-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="77052-114">PARAMETERS</span></span>

### <span data-ttu-id="77052-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="77052-115">-Account</span></span>
<span data-ttu-id="77052-116">Gibt den Namen des Daten Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="77052-116">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="77052-117">-Ablauf</span><span class="sxs-lookup"><span data-stu-id="77052-117">-Expiration</span></span>
<span data-ttu-id="77052-118">Die absolute Ablaufzeit für die angegebene Datei.</span><span class="sxs-lookup"><span data-stu-id="77052-118">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="77052-119">Wenn kein Wert oder auf MaxValue gesetzt wird, läuft die Datei nie ab.</span><span class="sxs-lookup"><span data-stu-id="77052-119">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77052-120">-Path</span><span class="sxs-lookup"><span data-stu-id="77052-120">-Path</span></span>
<span data-ttu-id="77052-121">Gibt den Daten See-Speicherpfad für das Dateielement an, für das das Ablaufdatum festgelegt oder entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="77052-121">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

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

### <span data-ttu-id="77052-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="77052-122">-Confirm</span></span>
<span data-ttu-id="77052-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="77052-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77052-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77052-124">-WhatIf</span></span>
<span data-ttu-id="77052-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77052-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77052-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="77052-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77052-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77052-127">-DefaultProfile</span></span>
<span data-ttu-id="77052-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="77052-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77052-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77052-129">CommonParameters</span></span>
<span data-ttu-id="77052-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77052-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77052-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77052-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77052-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="77052-132">INPUTS</span></span>

## <span data-ttu-id="77052-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="77052-133">OUTPUTS</span></span>

### <span data-ttu-id="77052-134">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="77052-134">DataLakeStoreItem</span></span>
<span data-ttu-id="77052-135">Die aktualisierte Datei mit einer neuen Ablaufzeit.</span><span class="sxs-lookup"><span data-stu-id="77052-135">The updated file with a new expiration time.</span></span>

## <span data-ttu-id="77052-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="77052-136">NOTES</span></span>
<span data-ttu-id="77052-137">Alias: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="77052-137">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="77052-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="77052-138">RELATED LINKS</span></span>

[<span data-ttu-id="77052-139">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="77052-139">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

