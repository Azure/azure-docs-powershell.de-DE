---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: f435715c4c9361fcd396c751ea6956bfcffe1c1d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297843"
---
# <span data-ttu-id="d5bc6-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="d5bc6-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="d5bc6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d5bc6-102">SYNOPSIS</span></span>
<span data-ttu-id="d5bc6-103">Ruft die oktale Berechtigung einer Datei oder eines Ordners im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d5bc6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5bc6-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5bc6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5bc6-105">DESCRIPTION</span></span>
<span data-ttu-id="d5bc6-106">Das Cmdlet " **Get-AzDataLakeStoreItemPermission** " Ruft die oktale Berechtigung einer Datei oder eines Ordners im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d5bc6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5bc6-107">EXAMPLES</span></span>

### <span data-ttu-id="d5bc6-108">Beispiel 1: Legen Sie die Berechtigung Oktal für eine Datei</span><span class="sxs-lookup"><span data-stu-id="d5bc6-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="d5bc6-109">Dieser Befehl ruft die Berechtigung Oktal für eine Datei ab.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="d5bc6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5bc6-110">PARAMETERS</span></span>

### <span data-ttu-id="d5bc6-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="d5bc6-111">-Account</span></span>
<span data-ttu-id="d5bc6-112">Gibt den Namen des Daten Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="d5bc6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5bc6-113">-DefaultProfile</span></span>
<span data-ttu-id="d5bc6-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5bc6-115">-Path</span><span class="sxs-lookup"><span data-stu-id="d5bc6-115">-Path</span></span>
<span data-ttu-id="d5bc6-116">Gibt den Daten See-Speicherpfad der Datei oder des Ordners an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="d5bc6-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d5bc6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5bc6-117">CommonParameters</span></span>
<span data-ttu-id="d5bc6-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5bc6-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5bc6-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5bc6-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d5bc6-120">INPUTS</span></span>

### <span data-ttu-id="d5bc6-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d5bc6-121">System.String</span></span>

### <span data-ttu-id="d5bc6-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d5bc6-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="d5bc6-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d5bc6-123">OUTPUTS</span></span>

### <span data-ttu-id="d5bc6-124">System. String</span><span class="sxs-lookup"><span data-stu-id="d5bc6-124">System.String</span></span>

## <span data-ttu-id="d5bc6-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="d5bc6-125">NOTES</span></span>
* <span data-ttu-id="d5bc6-126">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="d5bc6-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="d5bc6-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d5bc6-127">RELATED LINKS</span></span>

[<span data-ttu-id="d5bc6-128">Satz-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="d5bc6-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


