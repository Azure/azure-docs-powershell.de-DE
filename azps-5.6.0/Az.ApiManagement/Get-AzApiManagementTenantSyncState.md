---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: d253c1da05bd62e40dcdddaa90033512b3932d27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945412"
---
# <span data-ttu-id="1da0f-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="1da0f-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="1da0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1da0f-102">SYNOPSIS</span></span>
<span data-ttu-id="1da0f-103">Ruft den Status der neuesten Synchronisierung zwischen der Konfigurationsdatenbank und dem Git-Repository ab.</span><span class="sxs-lookup"><span data-stu-id="1da0f-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="1da0f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1da0f-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1da0f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1da0f-105">DESCRIPTION</span></span>
<span data-ttu-id="1da0f-106">Das **Get-AzApiManagementTenantSyncState-Cmdlet** ruft den Status der neuesten Synchronisierung zwischen der Konfigurationsdatenbank und dem Git-Repository ab.</span><span class="sxs-lookup"><span data-stu-id="1da0f-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="1da0f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1da0f-107">EXAMPLES</span></span>

### <span data-ttu-id="1da0f-108">Beispiel 1: Anzeigen des Status der neuesten Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="1da0f-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="1da0f-109">Dieser Befehl ruft den Status der neuesten Synchronisierung zwischen der Konfigurationsdatenbank und dem Git-Repository ab.</span><span class="sxs-lookup"><span data-stu-id="1da0f-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="1da0f-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1da0f-110">PARAMETERS</span></span>

### <span data-ttu-id="1da0f-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1da0f-111">-Context</span></span>
<span data-ttu-id="1da0f-112">Gibt ein **PsApiManagementContext-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="1da0f-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1da0f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1da0f-113">-DefaultProfile</span></span>
<span data-ttu-id="1da0f-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1da0f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1da0f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1da0f-115">CommonParameters</span></span>
<span data-ttu-id="1da0f-116">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1da0f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1da0f-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1da0f-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1da0f-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1da0f-118">INPUTS</span></span>

### <span data-ttu-id="1da0f-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1da0f-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="1da0f-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1da0f-120">OUTPUTS</span></span>

### <span data-ttu-id="1da0f-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="1da0f-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="1da0f-122">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1da0f-122">NOTES</span></span>

## <span data-ttu-id="1da0f-123">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1da0f-123">RELATED LINKS</span></span>
