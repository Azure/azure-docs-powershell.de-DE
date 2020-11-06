---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 2e18be1721f68a0e1223bf45b9ca2e637c05a378
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498550"
---
# <span data-ttu-id="91e6e-101">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="91e6e-101">Get-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="91e6e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91e6e-102">SYNOPSIS</span></span>
<span data-ttu-id="91e6e-103">Ruft einen autorisierungsserver für die API-Verwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="91e6e-103">Gets an API Management authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91e6e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91e6e-104">SYNTAX</span></span>

### <span data-ttu-id="91e6e-105">GetAllAuthorizationServers (Standard)</span><span class="sxs-lookup"><span data-stu-id="91e6e-105">GetAllAuthorizationServers (Default)</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91e6e-106">GetByServerId</span><span class="sxs-lookup"><span data-stu-id="91e6e-106">GetByServerId</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91e6e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91e6e-107">DESCRIPTION</span></span>
<span data-ttu-id="91e6e-108">Das Cmdlet " **Get-AzureRmApiManagementAuthorizationServer** " ruft alle Azure API-Verwaltungs autorisierungsserver oder angegebenen autorisierungsserver ab.</span><span class="sxs-lookup"><span data-stu-id="91e6e-108">The **Get-AzureRmApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="91e6e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91e6e-109">EXAMPLES</span></span>

### <span data-ttu-id="91e6e-110">Beispiel 1: Abrufen aller autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="91e6e-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="91e6e-111">Dieser Befehl ruft alle autorisierungsserver für die API-Verwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="91e6e-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="91e6e-112">Beispiel 2: Abrufen eines angegebenen autorisierungsservers</span><span class="sxs-lookup"><span data-stu-id="91e6e-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="91e6e-113">Dieser Befehl ruft den angegebenen autorisierungsserver ab.</span><span class="sxs-lookup"><span data-stu-id="91e6e-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="91e6e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="91e6e-114">PARAMETERS</span></span>

### <span data-ttu-id="91e6e-115">-Context</span><span class="sxs-lookup"><span data-stu-id="91e6e-115">-Context</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91e6e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91e6e-116">-DefaultProfile</span></span>
<span data-ttu-id="91e6e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="91e6e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91e6e-118">-Server-Nr</span><span class="sxs-lookup"><span data-stu-id="91e6e-118">-ServerId</span></span>
```yaml
Type: System.String
Parameter Sets: GetByServerId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91e6e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91e6e-119">CommonParameters</span></span>
<span data-ttu-id="91e6e-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91e6e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91e6e-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91e6e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91e6e-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91e6e-122">INPUTS</span></span>

### <span data-ttu-id="91e6e-123">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="91e6e-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="91e6e-124">System. String</span><span class="sxs-lookup"><span data-stu-id="91e6e-124">System.String</span></span>

## <span data-ttu-id="91e6e-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91e6e-125">OUTPUTS</span></span>

### <span data-ttu-id="91e6e-126">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="91e6e-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="91e6e-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="91e6e-127">NOTES</span></span>

## <span data-ttu-id="91e6e-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91e6e-128">RELATED LINKS</span></span>

[<span data-ttu-id="91e6e-129">Neu – AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="91e6e-129">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="91e6e-130">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="91e6e-130">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="91e6e-131">Satz-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="91e6e-131">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


