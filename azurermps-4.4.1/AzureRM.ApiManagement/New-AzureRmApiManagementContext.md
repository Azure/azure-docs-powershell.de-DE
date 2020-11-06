---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
ms.openlocfilehash: 7bf97454fd7dc4a2debc8861766981f6428f0b28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498054"
---
# <span data-ttu-id="d1352-101">New-AzureRmApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d1352-101">New-AzureRmApiManagementContext</span></span>

## <span data-ttu-id="d1352-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1352-102">SYNOPSIS</span></span>
<span data-ttu-id="d1352-103">Erstellt eine Instanz von PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d1352-103">Creates an instance of PsAzureApiManagementContext.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1352-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1352-104">SYNTAX</span></span>

```
New-AzureRmApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1352-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1352-105">DESCRIPTION</span></span>
<span data-ttu-id="d1352-106">Das Cmdlet **New-AzureRmApiManagementContext** erstellt eine Instanz von **PsAzureApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="d1352-106">The **New-AzureRmApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="d1352-107">Der Kontext wird für alle Cmdlets des API-Verwaltungsdiensts verwendet.</span><span class="sxs-lookup"><span data-stu-id="d1352-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="d1352-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1352-108">EXAMPLES</span></span>

### <span data-ttu-id="d1352-109">Beispiel 1: Erstellen einer PsApiManagementContext-Instanz</span><span class="sxs-lookup"><span data-stu-id="d1352-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="d1352-110">Dieser Befehl erstellt eine Instanz von **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="d1352-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="d1352-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1352-111">PARAMETERS</span></span>

### <span data-ttu-id="d1352-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1352-112">-ResourceGroupName</span></span>
<span data-ttu-id="d1352-113">Gibt den Namen der Ressourcengruppe an, unter der ein API-Verwaltungsdienst bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d1352-113">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1352-114">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d1352-114">-ServiceName</span></span>
<span data-ttu-id="d1352-115">Gibt den Namen des bereitgestellten API-Verwaltungsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="d1352-115">Specifies the name of the deployed API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1352-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1352-116">-DefaultProfile</span></span>
<span data-ttu-id="d1352-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d1352-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1352-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1352-118">CommonParameters</span></span>
<span data-ttu-id="d1352-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1352-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1352-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1352-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1352-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1352-121">INPUTS</span></span>

## <span data-ttu-id="d1352-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1352-122">OUTPUTS</span></span>

### <span data-ttu-id="d1352-123">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsAzureApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d1352-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsAzureApiManagementContext</span></span>

## <span data-ttu-id="d1352-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1352-124">NOTES</span></span>

## <span data-ttu-id="d1352-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1352-125">RELATED LINKS</span></span>

