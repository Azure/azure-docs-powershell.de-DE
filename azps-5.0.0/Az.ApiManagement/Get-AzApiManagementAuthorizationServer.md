---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ad06e1f9c37920c2362db3a94cdfbace91bf3796
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302253"
---
# <span data-ttu-id="9d371-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="9d371-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="9d371-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d371-102">SYNOPSIS</span></span>
<span data-ttu-id="9d371-103">Ruft einen autorisierungsserver für die API-Verwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="9d371-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="9d371-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d371-104">SYNTAX</span></span>

### <span data-ttu-id="9d371-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9d371-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d371-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d371-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d371-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d371-107">DESCRIPTION</span></span>
<span data-ttu-id="9d371-108">Das Cmdlet " **Get-AzApiManagementAuthorizationServer** " ruft alle Azure API-Verwaltungs autorisierungsserver oder den angegebenen autorisierungsserver ab.</span><span class="sxs-lookup"><span data-stu-id="9d371-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization server.</span></span>
<span data-ttu-id="9d371-109">ClientSecret wird nicht in Ergebnisdetails eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="9d371-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="9d371-110">Verwenden **Sie Get-AzApiManagementAuthorizationServerClientSecret** , um Client Secret zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9d371-110">To get client secret, use **Get-AzApiManagementAuthorizationServerClientSecret**.</span></span>

## <span data-ttu-id="9d371-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d371-111">EXAMPLES</span></span>

### <span data-ttu-id="9d371-112">Beispiel 1: Abrufen aller autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="9d371-112">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="9d371-113">Dieser Befehl ruft alle autorisierungsserver für die API-Verwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="9d371-113">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="9d371-114">Beispiel 2: Abrufen eines angegebenen autorisierungsservers</span><span class="sxs-lookup"><span data-stu-id="9d371-114">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="9d371-115">Dieser Befehl ruft den angegebenen autorisierungsserver ab.</span><span class="sxs-lookup"><span data-stu-id="9d371-115">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="9d371-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d371-116">PARAMETERS</span></span>

### <span data-ttu-id="9d371-117">-Context</span><span class="sxs-lookup"><span data-stu-id="9d371-117">-Context</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d371-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d371-118">-DefaultProfile</span></span>
<span data-ttu-id="9d371-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9d371-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d371-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9d371-120">-ResourceId</span></span>
<span data-ttu-id="9d371-121">Arm-Ressourcenbezeichner des autorisierungsservers.</span><span class="sxs-lookup"><span data-stu-id="9d371-121">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="9d371-122">Wenn angegeben, wird versucht, den autorisierungsserver anhand des Bezeichners zu finden.</span><span class="sxs-lookup"><span data-stu-id="9d371-122">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="9d371-123">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9d371-123">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d371-124">-Server-Nr</span><span class="sxs-lookup"><span data-stu-id="9d371-124">-ServerId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d371-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d371-125">CommonParameters</span></span>
<span data-ttu-id="9d371-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d371-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d371-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d371-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d371-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d371-128">INPUTS</span></span>

### <span data-ttu-id="9d371-129">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9d371-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9d371-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9d371-130">System.String</span></span>

## <span data-ttu-id="9d371-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d371-131">OUTPUTS</span></span>

### <span data-ttu-id="9d371-132">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="9d371-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="9d371-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d371-133">NOTES</span></span>

## <span data-ttu-id="9d371-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d371-134">RELATED LINKS</span></span>

[<span data-ttu-id="9d371-135">Neu – AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="9d371-135">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="9d371-136">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="9d371-136">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="9d371-137">Satz-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="9d371-137">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


