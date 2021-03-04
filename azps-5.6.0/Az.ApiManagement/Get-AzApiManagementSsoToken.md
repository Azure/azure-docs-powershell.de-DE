---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: eae199f28314db5aa50fa3247b46f02a407802fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945443"
---
# <span data-ttu-id="af9f2-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="af9f2-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="af9f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af9f2-102">SYNOPSIS</span></span>
<span data-ttu-id="af9f2-103">Ruft einen Link mit einem SSO-Token zu einem bereitgestellten Verwaltungsportal eines API-Verwaltungsdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="af9f2-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="af9f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af9f2-104">SYNTAX</span></span>

### <span data-ttu-id="af9f2-105">ExpandedParameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="af9f2-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af9f2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="af9f2-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af9f2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af9f2-107">DESCRIPTION</span></span>
<span data-ttu-id="af9f2-108">Das **Get-AzApiManagementSsoToken-Cmdlet** gibt einen Link (URL) zurück, der ein SSO-Token (Single Sign-On) zu einem bereitgestellten Verwaltungsportal eines API-Verwaltungsdiensts enthält.</span><span class="sxs-lookup"><span data-stu-id="af9f2-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="af9f2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="af9f2-109">EXAMPLES</span></span>

### <span data-ttu-id="af9f2-110">Beispiel 1: Abrufen des SSO-Tokens eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="af9f2-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="af9f2-111">Dieser Befehl ruft das SSO-Token eines API-Verwaltungsdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="af9f2-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="af9f2-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="af9f2-112">PARAMETERS</span></span>

### <span data-ttu-id="af9f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af9f2-113">-DefaultProfile</span></span>
<span data-ttu-id="af9f2-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="af9f2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af9f2-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af9f2-115">-InputObject</span></span>
<span data-ttu-id="af9f2-116">Instanz von PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="af9f2-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="af9f2-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="af9f2-117">This parameter is required.</span></span>

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

### <span data-ttu-id="af9f2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="af9f2-118">-Name</span></span>
<span data-ttu-id="af9f2-119">Gibt den Namen der API-Verwaltungsinstanz an.</span><span class="sxs-lookup"><span data-stu-id="af9f2-119">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="af9f2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af9f2-120">-ResourceGroupName</span></span>
<span data-ttu-id="af9f2-121">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="af9f2-121">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="af9f2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af9f2-122">CommonParameters</span></span>
<span data-ttu-id="af9f2-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af9f2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af9f2-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af9f2-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af9f2-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="af9f2-125">INPUTS</span></span>

### <span data-ttu-id="af9f2-126">System.String</span><span class="sxs-lookup"><span data-stu-id="af9f2-126">System.String</span></span>

## <span data-ttu-id="af9f2-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="af9f2-127">OUTPUTS</span></span>

### <span data-ttu-id="af9f2-128">System.String</span><span class="sxs-lookup"><span data-stu-id="af9f2-128">System.String</span></span>

## <span data-ttu-id="af9f2-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="af9f2-129">NOTES</span></span>

## <span data-ttu-id="af9f2-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="af9f2-130">RELATED LINKS</span></span>

[<span data-ttu-id="af9f2-131">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="af9f2-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)


