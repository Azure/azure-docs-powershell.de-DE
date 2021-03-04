---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: ac03d161e8ea786b939f8068dc2efd9109af3ab5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928187"
---
# <span data-ttu-id="82717-101">Get-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="82717-101">Get-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="82717-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82717-102">SYNOPSIS</span></span>
<span data-ttu-id="82717-103">Ruft den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="82717-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="82717-104">Wenn kein Anbieter angegeben ist, werden alle Anbieter für das Konto aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="82717-104">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="82717-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82717-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82717-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82717-106">DESCRIPTION</span></span>
<span data-ttu-id="82717-107">Das **Get-AzDataLakeStoreTrustedIdProvider-Cmdlet** ruft den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="82717-107">The **Get-AzDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="82717-108">Wenn kein Anbieter angegeben ist, werden alle Anbieter für das Konto aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="82717-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="82717-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="82717-109">EXAMPLES</span></span>

### <span data-ttu-id="82717-110">Beispiel 1: Einen bestimmten Anbieter für vertrauenswürdige Identitäten erhalten</span><span class="sxs-lookup"><span data-stu-id="82717-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="82717-111">Gibt den Anbieter mit dem Namen "MyProvider" vom Konto "ContosoADL" zurück.</span><span class="sxs-lookup"><span data-stu-id="82717-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="82717-112">Beispiel 2: Auflisten aller Anbieter in einem Konto</span><span class="sxs-lookup"><span data-stu-id="82717-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="82717-113">Listet alle Anbieter unter dem Konto "ContosoADL" auf.</span><span class="sxs-lookup"><span data-stu-id="82717-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="82717-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="82717-114">PARAMETERS</span></span>

### <span data-ttu-id="82717-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="82717-115">-Account</span></span>
<span data-ttu-id="82717-116">Das Data Lake Store-Konto zum Abrufen des vertrauenswürdigen Identitätsanbieters aus</span><span class="sxs-lookup"><span data-stu-id="82717-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="82717-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82717-117">-DefaultProfile</span></span>
<span data-ttu-id="82717-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="82717-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82717-119">-Name</span><span class="sxs-lookup"><span data-stu-id="82717-119">-Name</span></span>
<span data-ttu-id="82717-120">Der Name des vertrauenswürdigen Identitätsanbieters, der abgerufen werden soll</span><span class="sxs-lookup"><span data-stu-id="82717-120">The name of the trusted identity provider to retrieve</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82717-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82717-121">-ResourceGroupName</span></span>
<span data-ttu-id="82717-122">Name der Ressourcengruppe, unter der der angegebene vertrauenswürdige Identitätsanbieter des angegebenen Kontos abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="82717-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82717-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82717-123">CommonParameters</span></span>
<span data-ttu-id="82717-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82717-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82717-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82717-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82717-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="82717-126">INPUTS</span></span>

### <span data-ttu-id="82717-127">System.String</span><span class="sxs-lookup"><span data-stu-id="82717-127">System.String</span></span>

## <span data-ttu-id="82717-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="82717-128">OUTPUTS</span></span>

### <span data-ttu-id="82717-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="82717-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="82717-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="82717-130">NOTES</span></span>

## <span data-ttu-id="82717-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="82717-131">RELATED LINKS</span></span>
