---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 7e2a655810c885245d3694fb63caa44c5b4119e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663108"
---
# <span data-ttu-id="59a6a-101">Get-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="59a6a-101">Get-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="59a6a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59a6a-102">SYNOPSIS</span></span>
<span data-ttu-id="59a6a-103">Ruft die konfigurierten Einstellungen des Sicherheits Arbeitsbereichs für ein Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="59a6a-103">Gets the configured security workspace settings on a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59a6a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59a6a-104">SYNTAX</span></span>

### <span data-ttu-id="59a6a-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="59a6a-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59a6a-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="59a6a-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59a6a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="59a6a-107">ResourceId</span></span>
```
Get-AzureRmSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59a6a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59a6a-108">DESCRIPTION</span></span>
<span data-ttu-id="59a6a-109">Mit diesem Cmdlet können Sie den konfigurierten Arbeitsbereich ermitteln, in dem die Sicherheitsdaten enthalten sind, die vom Sicherheits-Agent erfasst wurden, der in VMs innerhalb dieses Abonnements installiert ist.</span><span class="sxs-lookup"><span data-stu-id="59a6a-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="59a6a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59a6a-110">EXAMPLES</span></span>

### <span data-ttu-id="59a6a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="59a6a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="59a6a-112">Ruft die Arbeitsbereichseinstellungen für ein Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="59a6a-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="59a6a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="59a6a-113">PARAMETERS</span></span>

### <span data-ttu-id="59a6a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59a6a-114">-DefaultProfile</span></span>
<span data-ttu-id="59a6a-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="59a6a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59a6a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="59a6a-116">-Name</span></span>
<span data-ttu-id="59a6a-117">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="59a6a-117">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a6a-118">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="59a6a-118">-ResourceId</span></span>
<span data-ttu-id="59a6a-119">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="59a6a-119">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59a6a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59a6a-120">CommonParameters</span></span>
<span data-ttu-id="59a6a-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59a6a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59a6a-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59a6a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59a6a-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59a6a-123">INPUTS</span></span>

### <span data-ttu-id="59a6a-124">System. String</span><span class="sxs-lookup"><span data-stu-id="59a6a-124">System.String</span></span>

## <span data-ttu-id="59a6a-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59a6a-125">OUTPUTS</span></span>

### <span data-ttu-id="59a6a-126">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="59a6a-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="59a6a-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="59a6a-127">NOTES</span></span>

## <span data-ttu-id="59a6a-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59a6a-128">RELATED LINKS</span></span>
