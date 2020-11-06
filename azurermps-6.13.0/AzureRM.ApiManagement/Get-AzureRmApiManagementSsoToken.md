---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
ms.openlocfilehash: e0bce4f579b2000bc970e35ceb03da03fdffb211
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476394"
---
# <span data-ttu-id="c363d-101">Get-AzureRmApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="c363d-101">Get-AzureRmApiManagementSsoToken</span></span>

## <span data-ttu-id="c363d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c363d-102">SYNOPSIS</span></span>
<span data-ttu-id="c363d-103">Ruft einen Link mit einem SSO-Token zu einem bereitgestellten Verwaltungsportal eines API-Verwaltungsdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="c363d-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c363d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c363d-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c363d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c363d-105">DESCRIPTION</span></span>
<span data-ttu-id="c363d-106">Das Cmdlet " **Get-AzureRmApiManagementSsoToken** " gibt einen Link (URL) mit einem Single Sign-on (SSO)-Token zu einem bereitgestellten Verwaltungsportal eines API-Verwaltungsdiensts zurück.</span><span class="sxs-lookup"><span data-stu-id="c363d-106">The **Get-AzureRmApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="c363d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c363d-107">EXAMPLES</span></span>

### <span data-ttu-id="c363d-108">Beispiel 1: Abrufen des SSO-Tokens eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="c363d-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzureRmApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="c363d-109">Dieser Befehl ruft das SSO-Token eines API-Verwaltungsdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="c363d-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="c363d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c363d-110">PARAMETERS</span></span>

### <span data-ttu-id="c363d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c363d-111">-DefaultProfile</span></span>
<span data-ttu-id="c363d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c363d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c363d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c363d-113">-Name</span></span>
<span data-ttu-id="c363d-114">Gibt den Namen der API-Verwaltungsinstanz an.</span><span class="sxs-lookup"><span data-stu-id="c363d-114">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="c363d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c363d-115">-ResourceGroupName</span></span>
<span data-ttu-id="c363d-116">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c363d-116">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="c363d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c363d-117">CommonParameters</span></span>
<span data-ttu-id="c363d-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c363d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c363d-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c363d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c363d-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c363d-120">INPUTS</span></span>

### <span data-ttu-id="c363d-121">System. String</span><span class="sxs-lookup"><span data-stu-id="c363d-121">System.String</span></span>

## <span data-ttu-id="c363d-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c363d-122">OUTPUTS</span></span>

### <span data-ttu-id="c363d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c363d-123">System.String</span></span>

## <span data-ttu-id="c363d-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="c363d-124">NOTES</span></span>

## <span data-ttu-id="c363d-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c363d-125">RELATED LINKS</span></span>

[<span data-ttu-id="c363d-126">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="c363d-126">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


