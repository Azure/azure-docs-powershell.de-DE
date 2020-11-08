---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: ca4f0d39b0023d641e2f95ceb4eddf90f19a51f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007839"
---
# <span data-ttu-id="9305e-101">Get-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="9305e-101">Get-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="9305e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9305e-102">SYNOPSIS</span></span>
<span data-ttu-id="9305e-103">Ruft die konfigurierten Einstellungen des Sicherheits Arbeitsbereichs für ein Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="9305e-103">Gets the configured security workspace settings on a subscription.</span></span>

## <span data-ttu-id="9305e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9305e-104">SYNTAX</span></span>

### <span data-ttu-id="9305e-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="9305e-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9305e-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="9305e-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9305e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9305e-107">ResourceId</span></span>
```
Get-AzSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9305e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9305e-108">DESCRIPTION</span></span>
<span data-ttu-id="9305e-109">Mit diesem Cmdlet können Sie den konfigurierten Arbeitsbereich ermitteln, in dem die Sicherheitsdaten enthalten sind, die vom Sicherheits-Agent erfasst wurden, der in VMs innerhalb dieses Abonnements installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9305e-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="9305e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9305e-110">EXAMPLES</span></span>

### <span data-ttu-id="9305e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9305e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="9305e-112">Ruft die Arbeitsbereichseinstellungen für ein Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="9305e-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="9305e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9305e-113">PARAMETERS</span></span>

### <span data-ttu-id="9305e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9305e-114">-DefaultProfile</span></span>
<span data-ttu-id="9305e-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9305e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9305e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9305e-116">-Name</span></span>
<span data-ttu-id="9305e-117">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="9305e-117">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9305e-118">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9305e-118">-ResourceId</span></span>
<span data-ttu-id="9305e-119">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="9305e-119">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9305e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9305e-120">CommonParameters</span></span>
<span data-ttu-id="9305e-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9305e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9305e-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9305e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9305e-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9305e-123">INPUTS</span></span>

### <span data-ttu-id="9305e-124">System. String</span><span class="sxs-lookup"><span data-stu-id="9305e-124">System.String</span></span>

## <span data-ttu-id="9305e-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9305e-125">OUTPUTS</span></span>

### <span data-ttu-id="9305e-126">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="9305e-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="9305e-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="9305e-127">NOTES</span></span>

## <span data-ttu-id="9305e-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9305e-128">RELATED LINKS</span></span>
