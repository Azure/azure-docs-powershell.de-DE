---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ce401334b03620ac565c5dd3b737b7a2982575e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658328"
---
# <span data-ttu-id="337fe-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="337fe-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="337fe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="337fe-102">SYNOPSIS</span></span>
<span data-ttu-id="337fe-103">Ruft einen autorisierungsserver für die API-Verwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="337fe-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="337fe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="337fe-104">SYNTAX</span></span>

### <span data-ttu-id="337fe-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="337fe-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="337fe-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="337fe-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="337fe-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="337fe-107">DESCRIPTION</span></span>
<span data-ttu-id="337fe-108">Das Cmdlet " **Get-AzApiManagementAuthorizationServer** " ruft alle Azure API-Verwaltungs autorisierungsserver oder angegebenen autorisierungsserver ab.</span><span class="sxs-lookup"><span data-stu-id="337fe-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="337fe-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="337fe-109">EXAMPLES</span></span>

### <span data-ttu-id="337fe-110">Beispiel 1: Abrufen aller autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="337fe-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="337fe-111">Dieser Befehl ruft alle autorisierungsserver für die API-Verwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="337fe-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="337fe-112">Beispiel 2: Abrufen eines angegebenen autorisierungsservers</span><span class="sxs-lookup"><span data-stu-id="337fe-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="337fe-113">Dieser Befehl ruft den angegebenen autorisierungsserver ab.</span><span class="sxs-lookup"><span data-stu-id="337fe-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="337fe-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="337fe-114">PARAMETERS</span></span>

### <span data-ttu-id="337fe-115">-Context</span><span class="sxs-lookup"><span data-stu-id="337fe-115">-Context</span></span>

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

### <span data-ttu-id="337fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="337fe-116">-DefaultProfile</span></span>
<span data-ttu-id="337fe-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="337fe-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="337fe-118">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="337fe-118">-ResourceId</span></span>
<span data-ttu-id="337fe-119">Arm-Ressourcenbezeichner des autorisierungsservers.</span><span class="sxs-lookup"><span data-stu-id="337fe-119">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="337fe-120">Wenn angegeben, wird versucht, den autorisierungsserver anhand des Bezeichners zu finden.</span><span class="sxs-lookup"><span data-stu-id="337fe-120">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="337fe-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="337fe-121">This parameter is required.</span></span>

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

### <span data-ttu-id="337fe-122">-Server-Nr</span><span class="sxs-lookup"><span data-stu-id="337fe-122">-ServerId</span></span>
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

### <span data-ttu-id="337fe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="337fe-123">CommonParameters</span></span>
<span data-ttu-id="337fe-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="337fe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="337fe-125">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="337fe-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="337fe-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="337fe-126">INPUTS</span></span>

### <span data-ttu-id="337fe-127">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="337fe-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="337fe-128">System. String</span><span class="sxs-lookup"><span data-stu-id="337fe-128">System.String</span></span>

## <span data-ttu-id="337fe-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="337fe-129">OUTPUTS</span></span>

### <span data-ttu-id="337fe-130">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="337fe-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="337fe-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="337fe-131">NOTES</span></span>

## <span data-ttu-id="337fe-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="337fe-132">RELATED LINKS</span></span>

[<span data-ttu-id="337fe-133">Neu – AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="337fe-133">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="337fe-134">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="337fe-134">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="337fe-135">Satz-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="337fe-135">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


