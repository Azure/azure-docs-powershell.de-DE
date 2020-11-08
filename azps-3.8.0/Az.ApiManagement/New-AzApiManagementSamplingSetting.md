---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsamplingsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
ms.openlocfilehash: 61f046576c14b61a59b55c52dd69c3e72b2c839e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996919"
---
# <span data-ttu-id="8922d-101">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="8922d-101">New-AzApiManagementSamplingSetting</span></span>

## <span data-ttu-id="8922d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8922d-102">SYNOPSIS</span></span>
<span data-ttu-id="8922d-103">Erstellen einer neuen Sampling-Einstellung für die Diagnose</span><span class="sxs-lookup"><span data-stu-id="8922d-103">Create a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="8922d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8922d-104">SYNTAX</span></span>

```
New-AzApiManagementSamplingSetting [-SamplingType <String>] [-SamplingPercentage <Double>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8922d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8922d-105">DESCRIPTION</span></span>
<span data-ttu-id="8922d-106">Das Cmdlet **New-AzApiManagementSamplingSetting** erstellt eine neue Sampling-Einstellung für die Diagnose</span><span class="sxs-lookup"><span data-stu-id="8922d-106">The cmdlet **New-AzApiManagementSamplingSetting** creates a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="8922d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8922d-107">EXAMPLES</span></span>

### <span data-ttu-id="8922d-108">Beispiel 1: Erstellen einer einfachen Sampling-Einstellung</span><span class="sxs-lookup"><span data-stu-id="8922d-108">Example 1 : Create a basic Sampling setting</span></span>
```powershell
PS C:\> New-AzApiManagementSamplingSetting -SamplingType fixed -Percentage 100

SamplingType Percentage
------------ ----------
fixed               100
```

<span data-ttu-id="8922d-109">Erstellt eine Sampling-Einstellung des `Fixed` Typs mit Protokollierung für 100% der Anforderungen/Antworten</span><span class="sxs-lookup"><span data-stu-id="8922d-109">Creates a sampling setting of `Fixed` type with logging for 100% of the requests / responses</span></span>

## <span data-ttu-id="8922d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8922d-110">PARAMETERS</span></span>

### <span data-ttu-id="8922d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8922d-111">-DefaultProfile</span></span>
<span data-ttu-id="8922d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8922d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8922d-113">-SamplingPercentage</span><span class="sxs-lookup"><span data-stu-id="8922d-113">-SamplingPercentage</span></span>
<span data-ttu-id="8922d-114">Abtastrate für Sampling mit fester Rate.</span><span class="sxs-lookup"><span data-stu-id="8922d-114">Rate of Sampling for Fixed Rate Sampling.</span></span> <span data-ttu-id="8922d-115">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="8922d-115">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8922d-116">-Samplingtype</span><span class="sxs-lookup"><span data-stu-id="8922d-116">-SamplingType</span></span>
<span data-ttu-id="8922d-117">Der Typ des Samplings.</span><span class="sxs-lookup"><span data-stu-id="8922d-117">The Type of Sampling.</span></span>
<span data-ttu-id="8922d-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="8922d-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="8922d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8922d-119">CommonParameters</span></span>
<span data-ttu-id="8922d-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8922d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8922d-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8922d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8922d-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8922d-122">INPUTS</span></span>

### <span data-ttu-id="8922d-123">Keine</span><span class="sxs-lookup"><span data-stu-id="8922d-123">None</span></span>

## <span data-ttu-id="8922d-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8922d-124">OUTPUTS</span></span>

### <span data-ttu-id="8922d-125">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="8922d-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

## <span data-ttu-id="8922d-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="8922d-126">NOTES</span></span>

## <span data-ttu-id="8922d-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8922d-127">RELATED LINKS</span></span>

[<span data-ttu-id="8922d-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8922d-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="8922d-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8922d-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="8922d-130">Satz-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8922d-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="8922d-131">Neu – AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="8922d-131">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)
