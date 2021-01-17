---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: c0c659f195aa1104b14f41e4cbc82a1ad86a1b1f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471453"
---
# <span data-ttu-id="015fd-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="015fd-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="015fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="015fd-102">SYNOPSIS</span></span>
<span data-ttu-id="015fd-103">Ruft die Zugriffskonfiguration für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="015fd-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="015fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="015fd-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="015fd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="015fd-105">DESCRIPTION</span></span>
<span data-ttu-id="015fd-106">Das **Cmdlet "Get-AzApiManagementTenantAccess"** ruft die Mandantenzugriffskonfiguration für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="015fd-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>
<span data-ttu-id="015fd-107">Die Tasten werden nicht in die Ergebnisdetails eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="015fd-107">Keys will not be included into result details.</span></span> <span data-ttu-id="015fd-108">Verwenden Sie **"Get-AzApiManagementTenantAccessSecret",** um den geheimen Clientgeheimnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="015fd-108">To get client secret, use **Get-AzApiManagementTenantAccessSecret**.</span></span>

## <span data-ttu-id="015fd-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="015fd-109">EXAMPLES</span></span>

### <span data-ttu-id="015fd-110">Beispiel 1: Erhalten der Konfiguration für den Mandantenzugriff</span><span class="sxs-lookup"><span data-stu-id="015fd-110">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="015fd-111">Dieser Befehl ruft die Mandantenzugriffskonfiguration für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="015fd-111">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="015fd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="015fd-112">PARAMETERS</span></span>

### <span data-ttu-id="015fd-113">-Context</span><span class="sxs-lookup"><span data-stu-id="015fd-113">-Context</span></span>
<span data-ttu-id="015fd-114">Gibt ein **"PsApiManagementContext"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="015fd-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="015fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="015fd-115">-DefaultProfile</span></span>
<span data-ttu-id="015fd-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="015fd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="015fd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="015fd-117">CommonParameters</span></span>
<span data-ttu-id="015fd-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="015fd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="015fd-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="015fd-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="015fd-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="015fd-120">INPUTS</span></span>

### <span data-ttu-id="015fd-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="015fd-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="015fd-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="015fd-122">OUTPUTS</span></span>

### <span data-ttu-id="015fd-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="015fd-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="015fd-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="015fd-124">NOTES</span></span>

## <span data-ttu-id="015fd-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="015fd-125">RELATED LINKS</span></span>

[<span data-ttu-id="015fd-126">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="015fd-126">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


