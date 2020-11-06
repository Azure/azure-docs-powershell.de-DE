---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: 6aeae8333cc8aa5a394abfaba68dcc0d7fb732f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480341"
---
# <span data-ttu-id="34d88-101">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="34d88-101">Get-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="34d88-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="34d88-102">SYNOPSIS</span></span>
<span data-ttu-id="34d88-103">Ruft die oktale Berechtigung einer Datei oder eines Ordners im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="34d88-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34d88-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="34d88-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34d88-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34d88-105">DESCRIPTION</span></span>
<span data-ttu-id="34d88-106">Das Cmdlet " **Get-AzureRmDataLakeStoreItemPermission** " Ruft die oktale Berechtigung einer Datei oder eines Ordners im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="34d88-106">The **Get-AzureRmDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="34d88-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34d88-107">EXAMPLES</span></span>

### <span data-ttu-id="34d88-108">Beispiel 1: Legen Sie die Berechtigung Oktal für eine Datei</span><span class="sxs-lookup"><span data-stu-id="34d88-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="34d88-109">Dieser Befehl ruft die Berechtigung Oktal für eine Datei ab.</span><span class="sxs-lookup"><span data-stu-id="34d88-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="34d88-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="34d88-110">PARAMETERS</span></span>

### <span data-ttu-id="34d88-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="34d88-111">-Account</span></span>
<span data-ttu-id="34d88-112">Gibt den Namen des Daten Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="34d88-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="34d88-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34d88-113">-DefaultProfile</span></span>
<span data-ttu-id="34d88-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="34d88-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34d88-115">-Path</span><span class="sxs-lookup"><span data-stu-id="34d88-115">-Path</span></span>
<span data-ttu-id="34d88-116">Gibt den Daten See-Speicherpfad der Datei oder des Ordners an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="34d88-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="34d88-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34d88-117">CommonParameters</span></span>
<span data-ttu-id="34d88-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34d88-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34d88-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34d88-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34d88-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="34d88-120">INPUTS</span></span>

### <span data-ttu-id="34d88-121">System. String</span><span class="sxs-lookup"><span data-stu-id="34d88-121">System.String</span></span>

### <span data-ttu-id="34d88-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="34d88-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="34d88-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="34d88-123">OUTPUTS</span></span>

### <span data-ttu-id="34d88-124">System. String</span><span class="sxs-lookup"><span data-stu-id="34d88-124">System.String</span></span>
<span data-ttu-id="34d88-125">Die Zeichenfolgendarstellung des Besitz oktals</span><span class="sxs-lookup"><span data-stu-id="34d88-125">The string representation of the ownership octal</span></span>

## <span data-ttu-id="34d88-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="34d88-126">NOTES</span></span>
* <span data-ttu-id="34d88-127">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="34d88-127">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="34d88-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="34d88-128">RELATED LINKS</span></span>

[<span data-ttu-id="34d88-129">Satz-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="34d88-129">Set-AzureRmDataLakeStoreItemPermission</span></span>](./Set-AzureRmDataLakeStoreItemPermission.md)


