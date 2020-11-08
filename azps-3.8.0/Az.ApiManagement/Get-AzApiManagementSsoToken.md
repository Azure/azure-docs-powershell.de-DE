---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 25c2439c07c9fe0b611c5b845f56e1de04f4d375
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004861"
---
# <span data-ttu-id="a8abe-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="a8abe-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="a8abe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a8abe-102">SYNOPSIS</span></span>
<span data-ttu-id="a8abe-103">Ruft einen Link mit einem SSO-Token zu einem bereitgestellten Verwaltungsportal eines API-Verwaltungsdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="a8abe-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="a8abe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8abe-104">SYNTAX</span></span>

### <span data-ttu-id="a8abe-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="a8abe-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8abe-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a8abe-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8abe-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8abe-107">DESCRIPTION</span></span>
<span data-ttu-id="a8abe-108">Das Cmdlet " **Get-AzApiManagementSsoToken** " gibt einen Link (URL) mit einem Single Sign-on (SSO)-Token zu einem bereitgestellten Verwaltungsportal eines API-Verwaltungsdiensts zurück.</span><span class="sxs-lookup"><span data-stu-id="a8abe-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="a8abe-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8abe-109">EXAMPLES</span></span>

### <span data-ttu-id="a8abe-110">Beispiel 1: Abrufen des SSO-Tokens eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="a8abe-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="a8abe-111">Dieser Befehl ruft das SSO-Token eines API-Verwaltungsdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="a8abe-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="a8abe-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8abe-112">PARAMETERS</span></span>

### <span data-ttu-id="a8abe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8abe-113">-DefaultProfile</span></span>
<span data-ttu-id="a8abe-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a8abe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8abe-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a8abe-115">-InputObject</span></span>
<span data-ttu-id="a8abe-116">Instanz von PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="a8abe-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="a8abe-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a8abe-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8abe-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a8abe-118">-Name</span></span>
<span data-ttu-id="a8abe-119">Gibt den Namen der API-Verwaltungsinstanz an.</span><span class="sxs-lookup"><span data-stu-id="a8abe-119">Specifies the name of the API Management instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8abe-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8abe-120">-ResourceGroupName</span></span>
<span data-ttu-id="a8abe-121">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a8abe-121">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8abe-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8abe-122">CommonParameters</span></span>
<span data-ttu-id="a8abe-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8abe-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8abe-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8abe-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8abe-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a8abe-125">INPUTS</span></span>

### <span data-ttu-id="a8abe-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a8abe-126">System.String</span></span>

## <span data-ttu-id="a8abe-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a8abe-127">OUTPUTS</span></span>

### <span data-ttu-id="a8abe-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a8abe-128">System.String</span></span>

## <span data-ttu-id="a8abe-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="a8abe-129">NOTES</span></span>

## <span data-ttu-id="a8abe-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a8abe-130">RELATED LINKS</span></span>

[<span data-ttu-id="a8abe-131">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="a8abe-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)


