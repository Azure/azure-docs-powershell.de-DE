---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 8b8ac352819b9b3ec7cd655501c5bf8cfbba6816
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658301"
---
# <span data-ttu-id="b947c-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="b947c-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="b947c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b947c-102">SYNOPSIS</span></span>
<span data-ttu-id="b947c-103">Ruft einen Link mit einem SSO-Token zu einem bereitgestellten Verwaltungsportal eines API-Verwaltungsdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="b947c-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="b947c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b947c-104">SYNTAX</span></span>

### <span data-ttu-id="b947c-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="b947c-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b947c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b947c-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b947c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b947c-107">DESCRIPTION</span></span>
<span data-ttu-id="b947c-108">Das Cmdlet " **Get-AzApiManagementSsoToken** " gibt einen Link (URL) mit einem Single Sign-on (SSO)-Token zu einem bereitgestellten Verwaltungsportal eines API-Verwaltungsdiensts zurück.</span><span class="sxs-lookup"><span data-stu-id="b947c-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="b947c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b947c-109">EXAMPLES</span></span>

### <span data-ttu-id="b947c-110">Beispiel 1: Abrufen des SSO-Tokens eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="b947c-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="b947c-111">Dieser Befehl ruft das SSO-Token eines API-Verwaltungsdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="b947c-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="b947c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b947c-112">PARAMETERS</span></span>

### <span data-ttu-id="b947c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b947c-113">-DefaultProfile</span></span>
<span data-ttu-id="b947c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b947c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b947c-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b947c-115">-InputObject</span></span>
<span data-ttu-id="b947c-116">Instanz von PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="b947c-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="b947c-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b947c-117">This parameter is required.</span></span>

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

### <span data-ttu-id="b947c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b947c-118">-Name</span></span>
<span data-ttu-id="b947c-119">Gibt den Namen der API-Verwaltungsinstanz an.</span><span class="sxs-lookup"><span data-stu-id="b947c-119">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="b947c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b947c-120">-ResourceGroupName</span></span>
<span data-ttu-id="b947c-121">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b947c-121">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="b947c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b947c-122">CommonParameters</span></span>
<span data-ttu-id="b947c-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b947c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b947c-124">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b947c-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b947c-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b947c-125">INPUTS</span></span>

### <span data-ttu-id="b947c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b947c-126">System.String</span></span>

## <span data-ttu-id="b947c-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b947c-127">OUTPUTS</span></span>

### <span data-ttu-id="b947c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b947c-128">System.String</span></span>

## <span data-ttu-id="b947c-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="b947c-129">NOTES</span></span>

## <span data-ttu-id="b947c-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b947c-130">RELATED LINKS</span></span>

[<span data-ttu-id="b947c-131">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b947c-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)


