---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserverclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
ms.openlocfilehash: 19e49269a4ae07b39e7a2795636e51df75b54905
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302247"
---
# <span data-ttu-id="26a7f-101">Get-AzApiManagementAuthorizationServerClientSecret</span><span class="sxs-lookup"><span data-stu-id="26a7f-101">Get-AzApiManagementAuthorizationServerClientSecret</span></span>

## <span data-ttu-id="26a7f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="26a7f-102">SYNOPSIS</span></span>
<span data-ttu-id="26a7f-103">Ruft einen Client für die API-Verwaltungs autorisierungsserver-Verschlüsselung ab.</span><span class="sxs-lookup"><span data-stu-id="26a7f-103">Gets an API Management authorization server client secret.</span></span>

## <span data-ttu-id="26a7f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="26a7f-104">SYNTAX</span></span>

### <span data-ttu-id="26a7f-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="26a7f-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26a7f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26a7f-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26a7f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26a7f-107">DESCRIPTION</span></span>
<span data-ttu-id="26a7f-108">Das Cmdlet " **Get-AzApiManagementAuthorizationServerClientSecret** " Ruft den Client Schlüssel des Azure API-Verwaltungs autorisierungsservers ab.</span><span class="sxs-lookup"><span data-stu-id="26a7f-108">The **Get-AzApiManagementAuthorizationServerClientSecret** cmdlet gets the client secret of the Azure API Management authorization server.</span></span>

## <span data-ttu-id="26a7f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="26a7f-109">EXAMPLES</span></span>

### <span data-ttu-id="26a7f-110">Beispiel 1: Abrufen eines angegebenen autorisierungsserver-Client Geheimnisses nach ID</span><span class="sxs-lookup"><span data-stu-id="26a7f-110">Example 1: Get a specified authorization server client secret by id</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServerClientSecret -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="26a7f-111">Dieser Befehl ruft den angegebenen autorisierungsserver als vertraulich ab.</span><span class="sxs-lookup"><span data-stu-id="26a7f-111">This command gets the specified authorization server cient secret.</span></span>

## <span data-ttu-id="26a7f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="26a7f-112">PARAMETERS</span></span>

### <span data-ttu-id="26a7f-113">-Context</span><span class="sxs-lookup"><span data-stu-id="26a7f-113">-Context</span></span>
<span data-ttu-id="26a7f-114">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="26a7f-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="26a7f-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="26a7f-115">This parameter is required.</span></span>

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

### <span data-ttu-id="26a7f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26a7f-116">-DefaultProfile</span></span>
<span data-ttu-id="26a7f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="26a7f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26a7f-118">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="26a7f-118">-ResourceId</span></span>
<span data-ttu-id="26a7f-119">Arm-Ressourcenbezeichner des autorisierungsservers.</span><span class="sxs-lookup"><span data-stu-id="26a7f-119">Arm Resource Identifier of the authorization server.</span></span>
<span data-ttu-id="26a7f-120">Wenn angegeben, wird versucht, den autorisierungsserver anhand des Bezeichners zu finden.</span><span class="sxs-lookup"><span data-stu-id="26a7f-120">If specified will try to find authorization server by the identifier.</span></span>
<span data-ttu-id="26a7f-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="26a7f-121">This parameter is required.</span></span>

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

### <span data-ttu-id="26a7f-122">-Server-Nr</span><span class="sxs-lookup"><span data-stu-id="26a7f-122">-ServerId</span></span>
<span data-ttu-id="26a7f-123">Der Bezeichner des autorisierungsservers.</span><span class="sxs-lookup"><span data-stu-id="26a7f-123">Identifier of the authorization server.</span></span>
<span data-ttu-id="26a7f-124">Wenn angegeben, findet der autorisierungsserver den Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="26a7f-124">If specified will find authorization server by the identifier.</span></span>
<span data-ttu-id="26a7f-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="26a7f-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="26a7f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26a7f-126">CommonParameters</span></span>
<span data-ttu-id="26a7f-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26a7f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26a7f-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26a7f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26a7f-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="26a7f-129">INPUTS</span></span>

### <span data-ttu-id="26a7f-130">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="26a7f-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="26a7f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="26a7f-131">System.String</span></span>

## <span data-ttu-id="26a7f-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="26a7f-132">OUTPUTS</span></span>

### <span data-ttu-id="26a7f-133">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="26a7f-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="26a7f-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="26a7f-134">NOTES</span></span>

## <span data-ttu-id="26a7f-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="26a7f-135">RELATED LINKS</span></span>
