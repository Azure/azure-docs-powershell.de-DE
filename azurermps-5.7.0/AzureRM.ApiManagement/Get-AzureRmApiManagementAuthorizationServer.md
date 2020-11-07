---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 651ef4c0c44b7e3269eb300dcfa098c39415f77d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663494"
---
# <span data-ttu-id="715ad-101">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="715ad-101">Get-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="715ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="715ad-102">SYNOPSIS</span></span>
<span data-ttu-id="715ad-103">Ruft einen autorisierungsserver für die API-Verwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="715ad-103">Gets an API Management authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="715ad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="715ad-104">SYNTAX</span></span>

### <span data-ttu-id="715ad-105">GetAllAuthorizationServers (Standard)</span><span class="sxs-lookup"><span data-stu-id="715ad-105">GetAllAuthorizationServers (Default)</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="715ad-106">GetByServerId</span><span class="sxs-lookup"><span data-stu-id="715ad-106">GetByServerId</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="715ad-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="715ad-107">DESCRIPTION</span></span>
<span data-ttu-id="715ad-108">Das Cmdlet " **Get-AzureRmApiManagementAuthorizationServer** " ruft alle Azure API-Verwaltungs autorisierungsserver oder angegebenen autorisierungsserver ab.</span><span class="sxs-lookup"><span data-stu-id="715ad-108">The **Get-AzureRmApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="715ad-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="715ad-109">EXAMPLES</span></span>

### <span data-ttu-id="715ad-110">Beispiel 1: Abrufen aller autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="715ad-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="715ad-111">Dieser Befehl ruft alle autorisierungsserver für die API-Verwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="715ad-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="715ad-112">Beispiel 2: Abrufen eines angegebenen autorisierungsservers</span><span class="sxs-lookup"><span data-stu-id="715ad-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="715ad-113">Dieser Befehl ruft den angegebenen autorisierungsserver ab.</span><span class="sxs-lookup"><span data-stu-id="715ad-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="715ad-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="715ad-114">PARAMETERS</span></span>

### <span data-ttu-id="715ad-115">-Context</span><span class="sxs-lookup"><span data-stu-id="715ad-115">-Context</span></span>
```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="715ad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="715ad-116">-DefaultProfile</span></span>
<span data-ttu-id="715ad-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="715ad-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="715ad-118">-Server-Nr</span><span class="sxs-lookup"><span data-stu-id="715ad-118">-ServerId</span></span>
```yaml
Type: String
Parameter Sets: GetByServerId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="715ad-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="715ad-119">CommonParameters</span></span>
<span data-ttu-id="715ad-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="715ad-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="715ad-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="715ad-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="715ad-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="715ad-122">INPUTS</span></span>

### <span data-ttu-id="715ad-123">Keine</span><span class="sxs-lookup"><span data-stu-id="715ad-123">None</span></span>
<span data-ttu-id="715ad-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="715ad-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="715ad-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="715ad-125">OUTPUTS</span></span>

### <span data-ttu-id="715ad-126">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="715ad-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>
<span data-ttu-id="715ad-127">Die Details des autorisierungsservers in einem bestimmten API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="715ad-127">The details of the Authorization Server in a given Api Management service.</span></span>

### <span data-ttu-id="715ad-128">IList<Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOAuth2AuthrozationServer></span><span class="sxs-lookup"><span data-stu-id="715ad-128">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer></span></span>
<span data-ttu-id="715ad-129">Die Liste des autorisierungsservers in einem bestimmten API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="715ad-129">The list of Authorization Server in a given Api Management service.</span></span>

## <span data-ttu-id="715ad-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="715ad-130">NOTES</span></span>

## <span data-ttu-id="715ad-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="715ad-131">RELATED LINKS</span></span>

[<span data-ttu-id="715ad-132">Neu – AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="715ad-132">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="715ad-133">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="715ad-133">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="715ad-134">Satz-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="715ad-134">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


