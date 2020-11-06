---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: 4806c4c25ac6fecce4961ef5d4ffe44daa1ae8f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500621"
---
# <span data-ttu-id="c1b91-101">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="c1b91-101">Set-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="c1b91-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c1b91-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b91-103">Ändert den Besitzer einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c1b91-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1b91-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1b91-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1b91-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1b91-105">DESCRIPTION</span></span>
<span data-ttu-id="c1b91-106">Das Cmdlet " **Satz-AzureRmDataLakeStoreItemOwner** " ändert den Besitzer einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c1b91-106">The **Set-AzureRmDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c1b91-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1b91-107">EXAMPLES</span></span>

### <span data-ttu-id="c1b91-108">Beispiel 1: Einrichten des Besitzers für ein Element</span><span class="sxs-lookup"><span data-stu-id="c1b91-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="c1b91-109">Dieser Befehl legt den Besitzer für das Stammverzeichnis auf Patti Fuller fest.</span><span class="sxs-lookup"><span data-stu-id="c1b91-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="c1b91-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1b91-110">PARAMETERS</span></span>

### <span data-ttu-id="c1b91-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="c1b91-111">-Account</span></span>
<span data-ttu-id="c1b91-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="c1b91-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="c1b91-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1b91-113">-DefaultProfile</span></span>
<span data-ttu-id="c1b91-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c1b91-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1b91-115">-ID</span><span class="sxs-lookup"><span data-stu-id="c1b91-115">-Id</span></span>
<span data-ttu-id="c1b91-116">Gibt die Objekt-ID des AzureActive-Verzeichnis Benutzers, der Gruppe oder des Dienst Prinzipals an, der als Besitzer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c1b91-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1b91-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1b91-117">-PassThru</span></span>
<span data-ttu-id="c1b91-118">Gibt an, dass der resultierende aktualisierte Besitzer zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c1b91-118">Indicates the resulting updated owner should be returned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1b91-119">-Path</span><span class="sxs-lookup"><span data-stu-id="c1b91-119">-Path</span></span>
<span data-ttu-id="c1b91-120">Gibt den Daten See-Speicherpfad des zu ändernden Elements an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="c1b91-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c1b91-121">-Typ</span><span class="sxs-lookup"><span data-stu-id="c1b91-121">-Type</span></span>
<span data-ttu-id="c1b91-122">Gibt den Typ des festzulegenden Besitzers an.</span><span class="sxs-lookup"><span data-stu-id="c1b91-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="c1b91-123">Die zulässigen Werte für diesen Parameter sind: Benutzer und Gruppe.</span><span class="sxs-lookup"><span data-stu-id="c1b91-123">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Owner
Parameter Sets: (All)
Aliases: 
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1b91-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c1b91-124">-Confirm</span></span>
<span data-ttu-id="c1b91-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c1b91-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1b91-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1b91-126">-WhatIf</span></span>
<span data-ttu-id="c1b91-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1b91-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1b91-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1b91-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1b91-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b91-129">CommonParameters</span></span>
<span data-ttu-id="c1b91-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1b91-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b91-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1b91-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b91-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c1b91-132">INPUTS</span></span>

### <span data-ttu-id="c1b91-133">Keine</span><span class="sxs-lookup"><span data-stu-id="c1b91-133">None</span></span>
<span data-ttu-id="c1b91-134">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="c1b91-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c1b91-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c1b91-135">OUTPUTS</span></span>

### <span data-ttu-id="c1b91-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c1b91-136">string</span></span>
<span data-ttu-id="c1b91-137">Wenn passthru angegeben ist, wird der aktualisierte Besitzer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c1b91-137">If PassThru is specified, returns the updated owner.</span></span>

## <span data-ttu-id="c1b91-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="c1b91-138">NOTES</span></span>

## <span data-ttu-id="c1b91-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c1b91-139">RELATED LINKS</span></span>

[<span data-ttu-id="c1b91-140">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="c1b91-140">Get-AzureRmDataLakeStoreItemOwner</span></span>](./Get-AzureRmDataLakeStoreItemOwner.md)


