---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
ms.openlocfilehash: da9924624065937a0cb2d78160b1a12cb698a42d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483189"
---
# <span data-ttu-id="6e1f9-101">New-AzureRmApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6e1f9-101">New-AzureRmApiManagementContext</span></span>

## <span data-ttu-id="6e1f9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6e1f9-102">SYNOPSIS</span></span>
<span data-ttu-id="6e1f9-103">Erstellt eine Instanz von PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-103">Creates an instance of PsAzureApiManagementContext.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e1f9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e1f9-104">SYNTAX</span></span>

```
New-AzureRmApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e1f9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e1f9-105">DESCRIPTION</span></span>
<span data-ttu-id="6e1f9-106">Das Cmdlet **New-AzureRmApiManagementContext** erstellt eine Instanz von **PsAzureApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-106">The **New-AzureRmApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="6e1f9-107">Der Kontext wird für alle Cmdlets des API-Verwaltungsdiensts verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="6e1f9-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e1f9-108">EXAMPLES</span></span>

### <span data-ttu-id="6e1f9-109">Beispiel 1: Erstellen einer PsApiManagementContext-Instanz</span><span class="sxs-lookup"><span data-stu-id="6e1f9-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="6e1f9-110">Dieser Befehl erstellt eine Instanz von **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="6e1f9-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e1f9-111">PARAMETERS</span></span>

### <span data-ttu-id="6e1f9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e1f9-112">-DefaultProfile</span></span>
<span data-ttu-id="6e1f9-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e1f9-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e1f9-114">-ResourceGroupName</span></span>
<span data-ttu-id="6e1f9-115">Gibt den Namen der Ressourcengruppe an, unter der ein API-Verwaltungsdienst bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-115">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e1f9-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6e1f9-116">-ServiceName</span></span>
<span data-ttu-id="6e1f9-117">Gibt den Namen des bereitgestellten API-Verwaltungsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-117">Specifies the name of the deployed API Management service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e1f9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e1f9-118">CommonParameters</span></span>
<span data-ttu-id="6e1f9-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e1f9-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e1f9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e1f9-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6e1f9-121">INPUTS</span></span>

### <span data-ttu-id="6e1f9-122">Keine</span><span class="sxs-lookup"><span data-stu-id="6e1f9-122">None</span></span>
<span data-ttu-id="6e1f9-123">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6e1f9-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6e1f9-124">OUTPUTS</span></span>

### <span data-ttu-id="6e1f9-125">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsAzureApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6e1f9-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsAzureApiManagementContext</span></span>

## <span data-ttu-id="6e1f9-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="6e1f9-126">NOTES</span></span>

## <span data-ttu-id="6e1f9-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6e1f9-127">RELATED LINKS</span></span>

