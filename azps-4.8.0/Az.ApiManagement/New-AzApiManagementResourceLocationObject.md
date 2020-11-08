---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementresourcelocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
ms.openlocfilehash: 505264809b513ad144fa3812193fc39f86ab9b1e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009441"
---
# <span data-ttu-id="e05d2-101">New-AzApiManagementResourceLocationObject</span><span class="sxs-lookup"><span data-stu-id="e05d2-101">New-AzApiManagementResourceLocationObject</span></span>

## <span data-ttu-id="e05d2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e05d2-102">SYNOPSIS</span></span>
<span data-ttu-id="e05d2-103">Erstellen eines neuen Ressourcen Standort Vertrags (wird in Gateways verwendet)</span><span class="sxs-lookup"><span data-stu-id="e05d2-103">Create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="e05d2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e05d2-104">SYNTAX</span></span>

```
New-AzApiManagementResourceLocationObject -Name <String> [-City <String>] [-District <String>]
 [-CountryOrRegion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e05d2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e05d2-105">DESCRIPTION</span></span>
<span data-ttu-id="e05d2-106">Das Cmdlet " **New-AzApiManagementResourceLocationObject** " erstellt einen neuen Ressourcen Standort Vertrag (wird in Gateways verwendet).</span><span class="sxs-lookup"><span data-stu-id="e05d2-106">The **New-AzApiManagementResourceLocationObject** cmdlet create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="e05d2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e05d2-107">EXAMPLES</span></span>

### <span data-ttu-id="e05d2-108">Beispiel 1: Erstellen eines Ressourcen Standort Vertrags</span><span class="sxs-lookup"><span data-stu-id="e05d2-108">Example 1: Create a resource location contract</span></span>
```powershell
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
```

<span data-ttu-id="e05d2-109">Dieser Befehl erstellt einen Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="e05d2-109">This command creates a resource location.</span></span>

## <span data-ttu-id="e05d2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e05d2-110">PARAMETERS</span></span>

### <span data-ttu-id="e05d2-111">-Ort</span><span class="sxs-lookup"><span data-stu-id="e05d2-111">-City</span></span>
<span data-ttu-id="e05d2-112">Standort Ort.</span><span class="sxs-lookup"><span data-stu-id="e05d2-112">Location City.</span></span>
<span data-ttu-id="e05d2-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e05d2-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05d2-114">-Land</span><span class="sxs-lookup"><span data-stu-id="e05d2-114">-CountryOrRegion</span></span>
<span data-ttu-id="e05d2-115">Standort Land oder Region.</span><span class="sxs-lookup"><span data-stu-id="e05d2-115">Location Country or Region.</span></span>
<span data-ttu-id="e05d2-116">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e05d2-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05d2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e05d2-117">-DefaultProfile</span></span>
<span data-ttu-id="e05d2-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e05d2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e05d2-119">-Distrikt</span><span class="sxs-lookup"><span data-stu-id="e05d2-119">-District</span></span>
<span data-ttu-id="e05d2-120">Ortsbezirk.</span><span class="sxs-lookup"><span data-stu-id="e05d2-120">Location District.</span></span>
<span data-ttu-id="e05d2-121">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e05d2-121">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05d2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e05d2-122">-Name</span></span>
<span data-ttu-id="e05d2-123">Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="e05d2-123">Location Name.</span></span>
<span data-ttu-id="e05d2-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e05d2-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05d2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e05d2-125">CommonParameters</span></span>
<span data-ttu-id="e05d2-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e05d2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e05d2-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e05d2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e05d2-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e05d2-128">INPUTS</span></span>

### <span data-ttu-id="e05d2-129">Keine</span><span class="sxs-lookup"><span data-stu-id="e05d2-129">None</span></span>

## <span data-ttu-id="e05d2-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e05d2-130">OUTPUTS</span></span>

### <span data-ttu-id="e05d2-131">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="e05d2-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="e05d2-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="e05d2-132">NOTES</span></span>

## <span data-ttu-id="e05d2-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e05d2-133">RELATED LINKS</span></span>
