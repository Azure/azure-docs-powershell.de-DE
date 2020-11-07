---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: 5270d77a9f9cd05b8075011e3fc002ac47d5c3a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651543"
---
# <span data-ttu-id="5960b-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="5960b-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="5960b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5960b-102">SYNOPSIS</span></span>
<span data-ttu-id="5960b-103">Ruft die oktale Berechtigung einer Datei oder eines Ordners im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="5960b-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="5960b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5960b-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5960b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5960b-105">DESCRIPTION</span></span>
<span data-ttu-id="5960b-106">Das Cmdlet " **Get-AzDataLakeStoreItemPermission** " Ruft die oktale Berechtigung einer Datei oder eines Ordners im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="5960b-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="5960b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5960b-107">EXAMPLES</span></span>

### <span data-ttu-id="5960b-108">Beispiel 1: Legen Sie die Berechtigung Oktal für eine Datei</span><span class="sxs-lookup"><span data-stu-id="5960b-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="5960b-109">Dieser Befehl ruft die Berechtigung Oktal für eine Datei ab.</span><span class="sxs-lookup"><span data-stu-id="5960b-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="5960b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5960b-110">PARAMETERS</span></span>

### <span data-ttu-id="5960b-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="5960b-111">-Account</span></span>
<span data-ttu-id="5960b-112">Gibt den Namen des Daten Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="5960b-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="5960b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5960b-113">-DefaultProfile</span></span>
<span data-ttu-id="5960b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5960b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5960b-115">-Path</span><span class="sxs-lookup"><span data-stu-id="5960b-115">-Path</span></span>
<span data-ttu-id="5960b-116">Gibt den Daten See-Speicherpfad der Datei oder des Ordners an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="5960b-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="5960b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5960b-117">CommonParameters</span></span>
<span data-ttu-id="5960b-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5960b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5960b-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5960b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5960b-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5960b-120">INPUTS</span></span>

### <span data-ttu-id="5960b-121">System. String</span><span class="sxs-lookup"><span data-stu-id="5960b-121">System.String</span></span>

### <span data-ttu-id="5960b-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="5960b-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="5960b-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5960b-123">OUTPUTS</span></span>

### <span data-ttu-id="5960b-124">System. String</span><span class="sxs-lookup"><span data-stu-id="5960b-124">System.String</span></span>

## <span data-ttu-id="5960b-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="5960b-125">NOTES</span></span>
* <span data-ttu-id="5960b-126">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="5960b-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="5960b-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5960b-127">RELATED LINKS</span></span>

[<span data-ttu-id="5960b-128">Satz-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="5960b-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


