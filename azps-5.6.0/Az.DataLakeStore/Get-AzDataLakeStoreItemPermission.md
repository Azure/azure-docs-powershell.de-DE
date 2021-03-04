---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: 0754160aa375ba84ac469771a97f792c36b51ce4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935272"
---
# <span data-ttu-id="a0d01-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="a0d01-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="a0d01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0d01-102">SYNOPSIS</span></span>
<span data-ttu-id="a0d01-103">Ruft die Berechtigung oktal einer Datei oder eines Ordners im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="a0d01-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a0d01-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0d01-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0d01-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0d01-105">DESCRIPTION</span></span>
<span data-ttu-id="a0d01-106">Das **Get-AzDataLakeStoreItemPermission-Cmdlet** erhält die Berechtigung oktal einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a0d01-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a0d01-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a0d01-107">EXAMPLES</span></span>

### <span data-ttu-id="a0d01-108">Beispiel 1: Festlegen der Oktalberechtigung für eine Datei</span><span class="sxs-lookup"><span data-stu-id="a0d01-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="a0d01-109">Dieser Befehl ruft die Berechtigung oktal für eine Datei ab.</span><span class="sxs-lookup"><span data-stu-id="a0d01-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="a0d01-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a0d01-110">PARAMETERS</span></span>

### <span data-ttu-id="a0d01-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="a0d01-111">-Account</span></span>
<span data-ttu-id="a0d01-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="a0d01-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="a0d01-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0d01-113">-DefaultProfile</span></span>
<span data-ttu-id="a0d01-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0d01-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0d01-115">-Path</span><span class="sxs-lookup"><span data-stu-id="a0d01-115">-Path</span></span>
<span data-ttu-id="a0d01-116">Gibt den Data Lake Store-Pfad der Datei oder des Ordners an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="a0d01-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="a0d01-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0d01-117">CommonParameters</span></span>
<span data-ttu-id="a0d01-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0d01-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0d01-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0d01-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0d01-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a0d01-120">INPUTS</span></span>

### <span data-ttu-id="a0d01-121">System.String</span><span class="sxs-lookup"><span data-stu-id="a0d01-121">System.String</span></span>

### <span data-ttu-id="a0d01-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="a0d01-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="a0d01-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a0d01-123">OUTPUTS</span></span>

### <span data-ttu-id="a0d01-124">System.String</span><span class="sxs-lookup"><span data-stu-id="a0d01-124">System.String</span></span>

## <span data-ttu-id="a0d01-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a0d01-125">NOTES</span></span>
* <span data-ttu-id="a0d01-126">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="a0d01-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="a0d01-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a0d01-127">RELATED LINKS</span></span>

[<span data-ttu-id="a0d01-128">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="a0d01-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


