---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: fb600edb4fd8d18ee82cb7f83d651e6588acaa42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458074"
---
# <span data-ttu-id="a9a49-101">Get-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="a9a49-101">Get-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="a9a49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9a49-102">SYNOPSIS</span></span>
<span data-ttu-id="a9a49-103">Ruft den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="a9a49-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="a9a49-104">Wenn kein Anbieter angegeben ist, werden alle Anbieter für das Konto aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9a49-104">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="a9a49-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9a49-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9a49-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9a49-106">DESCRIPTION</span></span>
<span data-ttu-id="a9a49-107">Das **Cmdlet "Get-AzDataLakeStoreTrustedIdProvider"** ruft den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="a9a49-107">The **Get-AzDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="a9a49-108">Wenn kein Anbieter angegeben ist, werden alle Anbieter für das Konto aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9a49-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="a9a49-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a9a49-109">EXAMPLES</span></span>

### <span data-ttu-id="a9a49-110">Beispiel 1: Einen bestimmten vertrauenswürdigen Identitätsanbieter erhalten</span><span class="sxs-lookup"><span data-stu-id="a9a49-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="a9a49-111">Gibt den Anbieter namens "MyProvider" aus dem Konto "ContosoADL" zurück.</span><span class="sxs-lookup"><span data-stu-id="a9a49-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="a9a49-112">Beispiel 2: Auflisten aller Anbieter in einem Konto</span><span class="sxs-lookup"><span data-stu-id="a9a49-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="a9a49-113">Listet alle Anbieter unter dem Konto "ContosoADL" auf.</span><span class="sxs-lookup"><span data-stu-id="a9a49-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="a9a49-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9a49-114">PARAMETERS</span></span>

### <span data-ttu-id="a9a49-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="a9a49-115">-Account</span></span>
<span data-ttu-id="a9a49-116">Das Data Lake Store-Konto, von dem der vertrauenswürdige Identitätsanbieter abgerufen werden soll</span><span class="sxs-lookup"><span data-stu-id="a9a49-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="a9a49-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9a49-117">-DefaultProfile</span></span>
<span data-ttu-id="a9a49-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a9a49-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9a49-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a9a49-119">-Name</span></span>
<span data-ttu-id="a9a49-120">Der Name des vertrauenswürdigen Identitätsanbieters, der abgerufen werden soll</span><span class="sxs-lookup"><span data-stu-id="a9a49-120">The name of the trusted identity provider to retrieve</span></span>

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

### <span data-ttu-id="a9a49-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9a49-121">-ResourceGroupName</span></span>
<span data-ttu-id="a9a49-122">Name der Ressourcengruppe, unter der der angegebene vertrauenswürdige Identitätsanbieter des angegebenen Kontos abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9a49-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

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

### <span data-ttu-id="a9a49-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9a49-123">CommonParameters</span></span>
<span data-ttu-id="a9a49-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9a49-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9a49-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9a49-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9a49-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a9a49-126">INPUTS</span></span>

### <span data-ttu-id="a9a49-127">System.String</span><span class="sxs-lookup"><span data-stu-id="a9a49-127">System.String</span></span>

## <span data-ttu-id="a9a49-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a9a49-128">OUTPUTS</span></span>

### <span data-ttu-id="a9a49-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="a9a49-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="a9a49-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a9a49-130">NOTES</span></span>

## <span data-ttu-id="a9a49-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a9a49-131">RELATED LINKS</span></span>
