---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: 05c5e797fa5ed56d6397b3881b368038a3d03a4f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661596"
---
# <span data-ttu-id="0c91c-101">Get-AzCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="0c91c-101">Get-AzCognitiveServicesAccountType</span></span>

## <span data-ttu-id="0c91c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0c91c-102">SYNOPSIS</span></span>
<span data-ttu-id="0c91c-103">Ruft die verfügbaren kognitiven Dienstkonto Typen ab.</span><span class="sxs-lookup"><span data-stu-id="0c91c-103">Gets the available Cognitive Services Account Types.</span></span>

## <span data-ttu-id="0c91c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c91c-104">SYNTAX</span></span>

### <span data-ttu-id="0c91c-105">GetAccountTypes (Standard)</span><span class="sxs-lookup"><span data-stu-id="0c91c-105">GetAccountTypes (Default)</span></span>
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c91c-106">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="0c91c-106">GetAccountTypeWithName</span></span>
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c91c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c91c-107">DESCRIPTION</span></span>
<span data-ttu-id="0c91c-108">Das Cmdlet " **Get-AzCognitiveServicesAccountType** " Ruft die verfügbaren kognitiven Dienstkonto Typen unter diesem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="0c91c-108">The **Get-AzCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="0c91c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c91c-109">EXAMPLES</span></span>

### <span data-ttu-id="0c91c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0c91c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

<span data-ttu-id="0c91c-111">Rufen Sie die Liste der verfügbaren Typen ab.</span><span class="sxs-lookup"><span data-stu-id="0c91c-111">Get the list of available Types.</span></span>

### <span data-ttu-id="0c91c-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0c91c-112">Example 2</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="0c91c-113">Rufen Sie die Liste der verfügbaren Typen in westus ab.</span><span class="sxs-lookup"><span data-stu-id="0c91c-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="0c91c-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="0c91c-114">Example 3</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="0c91c-115">Überprüfen Sie `Face` , ob es sich um einen gültigen Typnamen handelt, der Name wird zurückgegeben, wenn es sich um einen gültigen Namen handelt.</span><span class="sxs-lookup"><span data-stu-id="0c91c-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="0c91c-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c91c-116">PARAMETERS</span></span>

### <span data-ttu-id="0c91c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c91c-117">-DefaultProfile</span></span>
<span data-ttu-id="0c91c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0c91c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c91c-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="0c91c-119">-Location</span></span>
<span data-ttu-id="0c91c-120">Standort des kognitiven Dienstkontos</span><span class="sxs-lookup"><span data-stu-id="0c91c-120">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="0c91c-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="0c91c-121">-TypeName</span></span>
<span data-ttu-id="0c91c-122">Name des kognitiven Dienstkonto Typs</span><span class="sxs-lookup"><span data-stu-id="0c91c-122">Cognitive Services Account Type Name.</span></span>

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

### <span data-ttu-id="0c91c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c91c-123">CommonParameters</span></span>
<span data-ttu-id="0c91c-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c91c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c91c-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c91c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c91c-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0c91c-126">INPUTS</span></span>

### <span data-ttu-id="0c91c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0c91c-127">System.String</span></span>

## <span data-ttu-id="0c91c-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0c91c-128">OUTPUTS</span></span>

### <span data-ttu-id="0c91c-129">System. String []</span><span class="sxs-lookup"><span data-stu-id="0c91c-129">System.String[]</span></span>

### <span data-ttu-id="0c91c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0c91c-130">System.String</span></span>

## <span data-ttu-id="0c91c-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c91c-131">NOTES</span></span>

## <span data-ttu-id="0c91c-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0c91c-132">RELATED LINKS</span></span>
