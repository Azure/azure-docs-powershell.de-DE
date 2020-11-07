---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 40c9166ab650f7cb31ac53c55397bb7bc635f6e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650368"
---
# <span data-ttu-id="af84d-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="af84d-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="af84d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="af84d-102">SYNOPSIS</span></span>
<span data-ttu-id="af84d-103">Ruft einen Link mit einem SSO-Token zu einem bereitgestellten Verwaltungsportal eines API-Verwaltungsdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="af84d-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="af84d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="af84d-104">SYNTAX</span></span>

```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af84d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="af84d-105">DESCRIPTION</span></span>
<span data-ttu-id="af84d-106">Das Cmdlet " **Get-AzApiManagementSsoToken** " gibt einen Link (URL) mit einem Single Sign-on (SSO)-Token zu einem bereitgestellten Verwaltungsportal eines API-Verwaltungsdiensts zurück.</span><span class="sxs-lookup"><span data-stu-id="af84d-106">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="af84d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="af84d-107">EXAMPLES</span></span>

### <span data-ttu-id="af84d-108">Beispiel 1: Abrufen des SSO-Tokens eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="af84d-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="af84d-109">Dieser Befehl ruft das SSO-Token eines API-Verwaltungsdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="af84d-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="af84d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="af84d-110">PARAMETERS</span></span>

### <span data-ttu-id="af84d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af84d-111">-DefaultProfile</span></span>
<span data-ttu-id="af84d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="af84d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af84d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="af84d-113">-Name</span></span>
<span data-ttu-id="af84d-114">Gibt den Namen der API-Verwaltungsinstanz an.</span><span class="sxs-lookup"><span data-stu-id="af84d-114">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="af84d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af84d-115">-ResourceGroupName</span></span>
<span data-ttu-id="af84d-116">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="af84d-116">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="af84d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af84d-117">CommonParameters</span></span>
<span data-ttu-id="af84d-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af84d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af84d-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af84d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af84d-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="af84d-120">INPUTS</span></span>

### <span data-ttu-id="af84d-121">System. String</span><span class="sxs-lookup"><span data-stu-id="af84d-121">System.String</span></span>

## <span data-ttu-id="af84d-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="af84d-122">OUTPUTS</span></span>

### <span data-ttu-id="af84d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="af84d-123">System.String</span></span>

## <span data-ttu-id="af84d-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="af84d-124">NOTES</span></span>

## <span data-ttu-id="af84d-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="af84d-125">RELATED LINKS</span></span>

[<span data-ttu-id="af84d-126">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="af84d-126">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)


