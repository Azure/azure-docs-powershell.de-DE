---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
ms.openlocfilehash: 05a4af3e92febcf30d44de9b114972a7c1f61d5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501173"
---
# <span data-ttu-id="4742e-101">Get-AzureRmCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="4742e-101">Get-AzureRmCognitiveServicesAccountType</span></span>

## <span data-ttu-id="4742e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4742e-102">SYNOPSIS</span></span>
<span data-ttu-id="4742e-103">Ruft die verfügbaren kognitiven Dienstkonto Typen ab.</span><span class="sxs-lookup"><span data-stu-id="4742e-103">Gets the available Cognitive Services Account Types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4742e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4742e-104">SYNTAX</span></span>

### <span data-ttu-id="4742e-105">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="4742e-105">GetAccountTypeWithName</span></span>
```
Get-AzureRmCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4742e-106">GetAccountTypes</span><span class="sxs-lookup"><span data-stu-id="4742e-106">GetAccountTypes</span></span>
```
Get-AzureRmCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4742e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4742e-107">DESCRIPTION</span></span>
<span data-ttu-id="4742e-108">Das Cmdlet " **Get-AzureRmCognitiveServicesAccountType** " Ruft die verfügbaren kognitiven Dienstkonto Typen unter diesem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="4742e-108">The **Get-AzureRmCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="4742e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4742e-109">EXAMPLES</span></span>

### <span data-ttu-id="4742e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4742e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType
```

<span data-ttu-id="4742e-111">Rufen Sie die Liste der verfügbaren Typen ab.</span><span class="sxs-lookup"><span data-stu-id="4742e-111">Get the list of available Types.</span></span>

### <span data-ttu-id="4742e-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4742e-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="4742e-113">Rufen Sie die Liste der verfügbaren Typen in westus ab.</span><span class="sxs-lookup"><span data-stu-id="4742e-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="4742e-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4742e-114">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="4742e-115">Überprüfen Sie `Face` , ob es sich um einen gültigen Typnamen handelt, der Name wird zurückgegeben, wenn es sich um einen gültigen Namen handelt.</span><span class="sxs-lookup"><span data-stu-id="4742e-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="4742e-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="4742e-116">PARAMETERS</span></span>

### <span data-ttu-id="4742e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4742e-117">-DefaultProfile</span></span>
<span data-ttu-id="4742e-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4742e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4742e-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="4742e-119">-Location</span></span>
<span data-ttu-id="4742e-120">Standort des kognitiven Dienstkontos</span><span class="sxs-lookup"><span data-stu-id="4742e-120">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypes
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4742e-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="4742e-121">-TypeName</span></span>
<span data-ttu-id="4742e-122">Name des kognitiven Dienstkonto Typs</span><span class="sxs-lookup"><span data-stu-id="4742e-122">Cognitive Services Account Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypeWithName
Aliases: CognitiveServicesAccountTypeName, AccountTypeName, KindName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4742e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4742e-123">CommonParameters</span></span>
<span data-ttu-id="4742e-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4742e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4742e-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4742e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4742e-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4742e-126">INPUTS</span></span>

### <span data-ttu-id="4742e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4742e-127">System.String</span></span>

## <span data-ttu-id="4742e-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4742e-128">OUTPUTS</span></span>

### <span data-ttu-id="4742e-129">System. String []</span><span class="sxs-lookup"><span data-stu-id="4742e-129">System.String[]</span></span>

### <span data-ttu-id="4742e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4742e-130">System.String</span></span>

## <span data-ttu-id="4742e-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="4742e-131">NOTES</span></span>

## <span data-ttu-id="4742e-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4742e-132">RELATED LINKS</span></span>
