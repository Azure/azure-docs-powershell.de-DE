---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: 64af120d793719d4bcd6a24cc3d480cc8f6c104f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651546"
---
# <span data-ttu-id="08956-101">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="08956-101">Get-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="08956-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08956-102">SYNOPSIS</span></span>
<span data-ttu-id="08956-103">Ruft den Besitzer einer Datei oder eines Ordners im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="08956-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="08956-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08956-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08956-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08956-105">DESCRIPTION</span></span>
<span data-ttu-id="08956-106">Das Cmdlet " **Get-AzDataLakeStoreItemOwner** " Ruft den Besitzer einer Datei oder eines Ordners im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="08956-106">The **Get-AzDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="08956-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08956-107">EXAMPLES</span></span>

### <span data-ttu-id="08956-108">Beispiel 1: Abrufen des Besitzers für ein Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="08956-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="08956-109">Mit diesem Befehl wird der Benutzer Besitzer für das Stammverzeichnis des ContosoADL-Kontos abgerufen.</span><span class="sxs-lookup"><span data-stu-id="08956-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="08956-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="08956-110">PARAMETERS</span></span>

### <span data-ttu-id="08956-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="08956-111">-Account</span></span>
<span data-ttu-id="08956-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="08956-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="08956-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08956-113">-DefaultProfile</span></span>
<span data-ttu-id="08956-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="08956-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08956-115">-Path</span><span class="sxs-lookup"><span data-stu-id="08956-115">-Path</span></span>
<span data-ttu-id="08956-116">Gibt den Daten See-Speicherpfad eines Elements an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="08956-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="08956-117">-Typ</span><span class="sxs-lookup"><span data-stu-id="08956-117">-Type</span></span>
<span data-ttu-id="08956-118">Gibt den Typ des abzurufenden Besitzers an.</span><span class="sxs-lookup"><span data-stu-id="08956-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="08956-119">Die zulässigen Werte für diesen Parameter sind: Benutzer und Gruppe.</span><span class="sxs-lookup"><span data-stu-id="08956-119">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases:
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08956-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08956-120">CommonParameters</span></span>
<span data-ttu-id="08956-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08956-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08956-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08956-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08956-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08956-123">INPUTS</span></span>

### <span data-ttu-id="08956-124">System. String</span><span class="sxs-lookup"><span data-stu-id="08956-124">System.String</span></span>

### <span data-ttu-id="08956-125">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="08956-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="08956-126">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + Besitzer</span><span class="sxs-lookup"><span data-stu-id="08956-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="08956-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08956-127">OUTPUTS</span></span>

### <span data-ttu-id="08956-128">System. String</span><span class="sxs-lookup"><span data-stu-id="08956-128">System.String</span></span>

## <span data-ttu-id="08956-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="08956-129">NOTES</span></span>

## <span data-ttu-id="08956-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08956-130">RELATED LINKS</span></span>

[<span data-ttu-id="08956-131">Satz-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="08956-131">Set-AzDataLakeStoreItemOwner</span></span>](./Set-AzDataLakeStoreItemOwner.md)


