---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
ms.openlocfilehash: 927343f6a80edb82b933bfa382bbf6b690b90f07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483210"
---
# <span data-ttu-id="f0d35-101">Get-AzureRmApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="f0d35-101">Get-AzureRmApiManagementSsoToken</span></span>

## <span data-ttu-id="f0d35-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f0d35-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d35-103">Ruft einen Link mit einem SSO-Token zu einem bereitgestellten Verwaltungsportal eines API-Verwaltungsdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="f0d35-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0d35-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0d35-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0d35-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0d35-105">DESCRIPTION</span></span>
<span data-ttu-id="f0d35-106">Das Cmdlet " **Get-AzureRmApiManagementSsoToken** " gibt einen Link (URL) mit einem Single Sign-on (SSO)-Token zu einem bereitgestellten Verwaltungsportal eines API-Verwaltungsdiensts zurück.</span><span class="sxs-lookup"><span data-stu-id="f0d35-106">The **Get-AzureRmApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="f0d35-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f0d35-107">EXAMPLES</span></span>

### <span data-ttu-id="f0d35-108">Beispiel 1: Abrufen des SSO-Tokens eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="f0d35-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzureRmApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="f0d35-109">Dieser Befehl ruft das SSO-Token eines API-Verwaltungsdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="f0d35-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="f0d35-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0d35-110">PARAMETERS</span></span>

### <span data-ttu-id="f0d35-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d35-111">-DefaultProfile</span></span>
<span data-ttu-id="f0d35-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f0d35-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="f0d35-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f0d35-113">-Name</span></span>
<span data-ttu-id="f0d35-114">Gibt den Namen der API-Verwaltungsinstanz an.</span><span class="sxs-lookup"><span data-stu-id="f0d35-114">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="f0d35-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0d35-115">-ResourceGroupName</span></span>
<span data-ttu-id="f0d35-116">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f0d35-116">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="f0d35-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d35-117">CommonParameters</span></span>
<span data-ttu-id="f0d35-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0d35-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d35-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0d35-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d35-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f0d35-120">INPUTS</span></span>

### <span data-ttu-id="f0d35-121">Keine</span><span class="sxs-lookup"><span data-stu-id="f0d35-121">None</span></span>
<span data-ttu-id="f0d35-122">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f0d35-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f0d35-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f0d35-123">OUTPUTS</span></span>

### <span data-ttu-id="f0d35-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f0d35-124">System.String</span></span>

## <span data-ttu-id="f0d35-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="f0d35-125">NOTES</span></span>

## <span data-ttu-id="f0d35-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f0d35-126">RELATED LINKS</span></span>

[<span data-ttu-id="f0d35-127">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="f0d35-127">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


