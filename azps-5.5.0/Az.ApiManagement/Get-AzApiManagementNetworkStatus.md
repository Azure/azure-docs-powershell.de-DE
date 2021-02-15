---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnetworkstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNetworkStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNetworkStatus.md
ms.openlocfilehash: 5ba351ab1a5102acc1855e13821650b8ce1b4373
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159756"
---
# <span data-ttu-id="ea043-101">Get-AzApiManagementNetworkStatus</span><span class="sxs-lookup"><span data-stu-id="ea043-101">Get-AzApiManagementNetworkStatus</span></span>

## <span data-ttu-id="ea043-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea043-102">SYNOPSIS</span></span>
<span data-ttu-id="ea043-103">Ruft den Konnektivitätsstatus zu den externen Ressourcen ab, von denen der Api-Verwaltungsdienst innerhalb des Clouddiensts abhängt.</span><span class="sxs-lookup"><span data-stu-id="ea043-103">Gets the Connectivity Status to the external resources on which the Api Management service depends from inside the Cloud Service.</span></span> <span data-ttu-id="ea043-104">Dadurch werden auch die DNS-Server wie für CloudService sichtbar zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ea043-104">This also returns the DNS Servers as visible to the CloudService.</span></span>

## <span data-ttu-id="ea043-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea043-105">SYNTAX</span></span>

### <span data-ttu-id="ea043-106">ByInputObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="ea043-106">ByInputObject (Default)</span></span>
```
Get-AzApiManagementNetworkStatus -ApiManagementObject <PsApiManagement> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea043-107">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="ea043-107">ExpandedParameter</span></span>
```
Get-AzApiManagementNetworkStatus -ResourceGroupName <String> -Name <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea043-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea043-108">DESCRIPTION</span></span>
<span data-ttu-id="ea043-109">Ruft den Netzwerkstatus des api-Verwaltungsdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="ea043-109">Gets the Network status of their Api Management service</span></span>

## <span data-ttu-id="ea043-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ea043-110">EXAMPLES</span></span>

### <span data-ttu-id="ea043-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ea043-111">Example 1</span></span>
```powershell
PS D:\github\azure-powershell> Get-AzApiManagementNetworkStatus -ResourceGroupName powershelltest -Name powershellsdkservice

Location DnsServers      ConnectivityStatus
-------- ----------      ------------------
West US  {168.63.129.16} {apimgmtstaoonqs7wwzjosky.blob.core.windows.net, apimgmtstaoonqs7wwzjosky.file.core.windows.net, apimgmtstaoonqs7wwzjosky.queue.core.windows.net, apimgmtstaoonqs7wwzjosk...


PS D:\github\azure-powershell> $networkStatus = Get-AzApiManagementNetworkStatus -ResourceGroupName powershelltest -Name powershellsdkservice
PS D:\github\azure-powershell> $networkStatus.ConnectivityStatus


Name             : apimgmtstaoonqs7wwzjosky.blob.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : apimgmtstaoonqs7wwzjosky.file.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : apimgmtstaoonqs7wwzjosky.queue.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : apimgmtstaoonqs7wwzjosky.table.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : bx9gltecfv.database.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:41 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : https://prod3.metrics.nsatc.net:1886/RecoveryService
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:07:11 PM
LastStatusChange : 4/29/2019 1:31:30 PM

Name             : prod.warmpath.msftcloudes.com
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : Scm
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:04:27 PM
LastStatusChange : 4/30/2019 11:16:20 PM
```

<span data-ttu-id="ea043-112">Ruft den Verbindungsstatus der verschiedenen Ressourcen ab, von denen der ApiManagement-Dienst abhängt.</span><span class="sxs-lookup"><span data-stu-id="ea043-112">Gets the connectivity status of the different resources on which ApiManagement service depends upon.</span></span>

## <span data-ttu-id="ea043-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea043-113">PARAMETERS</span></span>

### <span data-ttu-id="ea043-114">-ApiManagementObject</span><span class="sxs-lookup"><span data-stu-id="ea043-114">-ApiManagementObject</span></span>
<span data-ttu-id="ea043-115">Instanz von PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ea043-115">Instance of PsApiManagement.</span></span> <span data-ttu-id="ea043-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ea043-116">This parameter is required.</span></span>

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

### <span data-ttu-id="ea043-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea043-117">-DefaultProfile</span></span>
<span data-ttu-id="ea043-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea043-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea043-119">-Location</span><span class="sxs-lookup"><span data-stu-id="ea043-119">-Location</span></span>
<span data-ttu-id="ea043-120">Speicherort des API-Verwaltungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="ea043-120">Location of the API Management Service.</span></span>

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

### <span data-ttu-id="ea043-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ea043-121">-Name</span></span>
<span data-ttu-id="ea043-122">Name der API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="ea043-122">Name of API Management.</span></span>

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

### <span data-ttu-id="ea043-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea043-123">-ResourceGroupName</span></span>
<span data-ttu-id="ea043-124">Name der Ressourcengruppe, unter der die API Management (API-Verwaltung) vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ea043-124">Name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="ea043-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea043-125">CommonParameters</span></span>
<span data-ttu-id="ea043-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea043-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea043-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea043-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea043-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ea043-128">INPUTS</span></span>

### <span data-ttu-id="ea043-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ea043-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="ea043-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ea043-130">System.String</span></span>

## <span data-ttu-id="ea043-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ea043-131">OUTPUTS</span></span>

### <span data-ttu-id="ea043-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementNetworkStatus</span><span class="sxs-lookup"><span data-stu-id="ea043-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementNetworkStatus</span></span>

## <span data-ttu-id="ea043-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ea043-133">NOTES</span></span>

## <span data-ttu-id="ea043-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ea043-134">RELATED LINKS</span></span>
