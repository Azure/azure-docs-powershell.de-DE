---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 25c2439c07c9fe0b611c5b845f56e1de04f4d375
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302842"
---
# <span data-ttu-id="eb7ce-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="eb7ce-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="eb7ce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eb7ce-102">SYNOPSIS</span></span>
<span data-ttu-id="eb7ce-103">Ruft einen Link mit einem SSO-Token zu einem bereitgestellten Verwaltungsportal eines API-Verwaltungsdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="eb7ce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb7ce-104">SYNTAX</span></span>

### <span data-ttu-id="eb7ce-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="eb7ce-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb7ce-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="eb7ce-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb7ce-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb7ce-107">DESCRIPTION</span></span>
<span data-ttu-id="eb7ce-108">Das Cmdlet " **Get-AzApiManagementSsoToken** " gibt einen Link (URL) mit einem Single Sign-on (SSO)-Token zu einem bereitgestellten Verwaltungsportal eines API-Verwaltungsdiensts zurück.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="eb7ce-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb7ce-109">EXAMPLES</span></span>

### <span data-ttu-id="eb7ce-110">Beispiel 1: Abrufen des SSO-Tokens eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="eb7ce-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="eb7ce-111">Dieser Befehl ruft das SSO-Token eines API-Verwaltungsdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="eb7ce-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb7ce-112">PARAMETERS</span></span>

### <span data-ttu-id="eb7ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb7ce-113">-DefaultProfile</span></span>
<span data-ttu-id="eb7ce-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb7ce-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="eb7ce-115">-InputObject</span></span>
<span data-ttu-id="eb7ce-116">Instanz von PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="eb7ce-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-117">This parameter is required.</span></span>

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

### <span data-ttu-id="eb7ce-118">-Name</span><span class="sxs-lookup"><span data-stu-id="eb7ce-118">-Name</span></span>
<span data-ttu-id="eb7ce-119">Gibt den Namen der API-Verwaltungsinstanz an.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-119">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="eb7ce-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb7ce-120">-ResourceGroupName</span></span>
<span data-ttu-id="eb7ce-121">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-121">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="eb7ce-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb7ce-122">CommonParameters</span></span>
<span data-ttu-id="eb7ce-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb7ce-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb7ce-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb7ce-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb7ce-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eb7ce-125">INPUTS</span></span>

### <span data-ttu-id="eb7ce-126">System. String</span><span class="sxs-lookup"><span data-stu-id="eb7ce-126">System.String</span></span>

## <span data-ttu-id="eb7ce-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eb7ce-127">OUTPUTS</span></span>

### <span data-ttu-id="eb7ce-128">System. String</span><span class="sxs-lookup"><span data-stu-id="eb7ce-128">System.String</span></span>

## <span data-ttu-id="eb7ce-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="eb7ce-129">NOTES</span></span>

## <span data-ttu-id="eb7ce-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eb7ce-130">RELATED LINKS</span></span>

[<span data-ttu-id="eb7ce-131">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb7ce-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)


