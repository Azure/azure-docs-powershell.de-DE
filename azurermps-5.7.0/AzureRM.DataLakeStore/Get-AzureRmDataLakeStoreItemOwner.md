---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: 886c8e7227d036e67d3e6f0d2dc04c4e9887e777
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481249"
---
# <span data-ttu-id="b62d1-101">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="b62d1-101">Get-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="b62d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b62d1-102">SYNOPSIS</span></span>
<span data-ttu-id="b62d1-103">Ruft den Besitzer einer Datei oder eines Ordners im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="b62d1-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b62d1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b62d1-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b62d1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b62d1-105">DESCRIPTION</span></span>
<span data-ttu-id="b62d1-106">Das Cmdlet " **Get-AzureRmDataLakeStoreItemOwner** " Ruft den Besitzer einer Datei oder eines Ordners im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="b62d1-106">The **Get-AzureRmDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b62d1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b62d1-107">EXAMPLES</span></span>

### <span data-ttu-id="b62d1-108">Beispiel 1: Abrufen des Besitzers für ein Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="b62d1-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="b62d1-109">Mit diesem Befehl wird der Benutzer Besitzer für das Stammverzeichnis des ContosoADL-Kontos abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b62d1-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="b62d1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b62d1-110">PARAMETERS</span></span>

### <span data-ttu-id="b62d1-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="b62d1-111">-Account</span></span>
<span data-ttu-id="b62d1-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="b62d1-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="b62d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b62d1-113">-DefaultProfile</span></span>
<span data-ttu-id="b62d1-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b62d1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b62d1-115">-Path</span><span class="sxs-lookup"><span data-stu-id="b62d1-115">-Path</span></span>
<span data-ttu-id="b62d1-116">Gibt den Daten See-Speicherpfad eines Elements an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="b62d1-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b62d1-117">-Typ</span><span class="sxs-lookup"><span data-stu-id="b62d1-117">-Type</span></span>
<span data-ttu-id="b62d1-118">Gibt den Typ des abzurufenden Besitzers an.</span><span class="sxs-lookup"><span data-stu-id="b62d1-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="b62d1-119">Die zulässigen Werte für diesen Parameter sind: Benutzer und Gruppe.</span><span class="sxs-lookup"><span data-stu-id="b62d1-119">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="b62d1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b62d1-120">CommonParameters</span></span>
<span data-ttu-id="b62d1-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b62d1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b62d1-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b62d1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b62d1-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b62d1-123">INPUTS</span></span>

### <span data-ttu-id="b62d1-124">Keine</span><span class="sxs-lookup"><span data-stu-id="b62d1-124">None</span></span>
<span data-ttu-id="b62d1-125">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="b62d1-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b62d1-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b62d1-126">OUTPUTS</span></span>

### <span data-ttu-id="b62d1-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b62d1-127">string</span></span>
<span data-ttu-id="b62d1-128">Der Besitzer des angegebenen Elements.</span><span class="sxs-lookup"><span data-stu-id="b62d1-128">The owner of the specified item.</span></span>

## <span data-ttu-id="b62d1-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="b62d1-129">NOTES</span></span>

## <span data-ttu-id="b62d1-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b62d1-130">RELATED LINKS</span></span>

[<span data-ttu-id="b62d1-131">Satz-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="b62d1-131">Set-AzureRmDataLakeStoreItemOwner</span></span>](./Set-AzureRmDataLakeStoreItemOwner.md)


