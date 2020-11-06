---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: f15ef7201622394a2b96964244980b059f1222c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476125"
---
# <span data-ttu-id="9acc1-101">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9acc1-101">Get-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="9acc1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9acc1-102">SYNOPSIS</span></span>
<span data-ttu-id="9acc1-103">Ruft Details zu einem Data Lake Store-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="9acc1-103">Gets details of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9acc1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9acc1-104">SYNTAX</span></span>

### <span data-ttu-id="9acc1-105">GetAllInSubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="9acc1-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9acc1-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9acc1-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9acc1-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="9acc1-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9acc1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9acc1-108">DESCRIPTION</span></span>
<span data-ttu-id="9acc1-109">Das Cmdlet " **Get-AzureRmDataLakeStoreAccount** " ruft Details zu einem Data Lake Store-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="9acc1-109">The **Get-AzureRmDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="9acc1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9acc1-110">EXAMPLES</span></span>

### <span data-ttu-id="9acc1-111">Beispiel 1: Abrufen eines Data Lake Store-Kontos</span><span class="sxs-lookup"><span data-stu-id="9acc1-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="9acc1-112">Dieser Befehl ruft das Konto mit dem Namen ContosoADL ab.</span><span class="sxs-lookup"><span data-stu-id="9acc1-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="9acc1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9acc1-113">PARAMETERS</span></span>

### <span data-ttu-id="9acc1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9acc1-114">-DefaultProfile</span></span>
<span data-ttu-id="9acc1-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9acc1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9acc1-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9acc1-116">-Name</span></span>
<span data-ttu-id="9acc1-117">Gibt den Namen des abzurufenden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="9acc1-117">Specifies the name of the account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9acc1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9acc1-118">-ResourceGroupName</span></span>
<span data-ttu-id="9acc1-119">Gibt den Namen der Ressourcengruppe an, die das abzurufende Data Lake Store-Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="9acc1-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9acc1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9acc1-120">CommonParameters</span></span>
<span data-ttu-id="9acc1-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9acc1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9acc1-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9acc1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9acc1-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9acc1-123">INPUTS</span></span>

### <span data-ttu-id="9acc1-124">System. String</span><span class="sxs-lookup"><span data-stu-id="9acc1-124">System.String</span></span>

## <span data-ttu-id="9acc1-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9acc1-125">OUTPUTS</span></span>

### <span data-ttu-id="9acc1-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9acc1-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="9acc1-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="9acc1-127">NOTES</span></span>

## <span data-ttu-id="9acc1-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9acc1-128">RELATED LINKS</span></span>

[<span data-ttu-id="9acc1-129">Neu – AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9acc1-129">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="9acc1-130">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9acc1-130">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="9acc1-131">Satz-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9acc1-131">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="9acc1-132">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9acc1-132">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


