---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: 654703a3c5cf1fc18e0f8fbb227b608e91c379bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936203"
---
# <span data-ttu-id="62ca8-101">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="62ca8-101">Get-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="62ca8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62ca8-102">SYNOPSIS</span></span>
<span data-ttu-id="62ca8-103">Ruft den Besitzer einer Datei oder eines Ordners im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="62ca8-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="62ca8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62ca8-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62ca8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62ca8-105">DESCRIPTION</span></span>
<span data-ttu-id="62ca8-106">Das **Get-AzDataLakeStoreItemOwner-Cmdlet** ruft den Besitzer einer Datei oder eines Ordners im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="62ca8-106">The **Get-AzDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="62ca8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="62ca8-107">EXAMPLES</span></span>

### <span data-ttu-id="62ca8-108">Beispiel 1: Den Besitzer für ein Verzeichnis erhalten</span><span class="sxs-lookup"><span data-stu-id="62ca8-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="62ca8-109">Dieser Befehl ruft den Benutzerbesitzer für das Stammverzeichnis des ContosoADL-Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="62ca8-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="62ca8-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="62ca8-110">PARAMETERS</span></span>

### <span data-ttu-id="62ca8-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="62ca8-111">-Account</span></span>
<span data-ttu-id="62ca8-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="62ca8-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="62ca8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62ca8-113">-DefaultProfile</span></span>
<span data-ttu-id="62ca8-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="62ca8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62ca8-115">-Path</span><span class="sxs-lookup"><span data-stu-id="62ca8-115">-Path</span></span>
<span data-ttu-id="62ca8-116">Gibt den Data Lake Store-Pfad eines Elements an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="62ca8-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="62ca8-117">-Type</span><span class="sxs-lookup"><span data-stu-id="62ca8-117">-Type</span></span>
<span data-ttu-id="62ca8-118">Gibt den Typ des zu erhaltenden Besitzers an.</span><span class="sxs-lookup"><span data-stu-id="62ca8-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="62ca8-119">Die zulässigen Werte für diesen Parameter sind: Benutzer und Gruppe.</span><span class="sxs-lookup"><span data-stu-id="62ca8-119">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="62ca8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62ca8-120">CommonParameters</span></span>
<span data-ttu-id="62ca8-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62ca8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62ca8-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62ca8-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62ca8-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="62ca8-123">INPUTS</span></span>

### <span data-ttu-id="62ca8-124">System.String</span><span class="sxs-lookup"><span data-stu-id="62ca8-124">System.String</span></span>

### <span data-ttu-id="62ca8-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="62ca8-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="62ca8-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span><span class="sxs-lookup"><span data-stu-id="62ca8-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="62ca8-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="62ca8-127">OUTPUTS</span></span>

### <span data-ttu-id="62ca8-128">System.String</span><span class="sxs-lookup"><span data-stu-id="62ca8-128">System.String</span></span>

## <span data-ttu-id="62ca8-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="62ca8-129">NOTES</span></span>

## <span data-ttu-id="62ca8-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="62ca8-130">RELATED LINKS</span></span>

[<span data-ttu-id="62ca8-131">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="62ca8-131">Set-AzDataLakeStoreItemOwner</span></span>](./Set-AzDataLakeStoreItemOwner.md)


