---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 98adc5714f4a4abaeca9fe6723b1a56fe1d49fca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664010"
---
# <span data-ttu-id="abb9f-101">Get-AzureRmSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="abb9f-101">Get-AzureRmSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="abb9f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="abb9f-102">SYNOPSIS</span></span>
<span data-ttu-id="abb9f-103">Ruft die Einstellungen für die automatische Bereitstellung der Sicherheit ab</span><span class="sxs-lookup"><span data-stu-id="abb9f-103">Gets the security automatic provisioning settings</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abb9f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="abb9f-104">SYNTAX</span></span>

### <span data-ttu-id="abb9f-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="abb9f-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abb9f-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="abb9f-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="abb9f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="abb9f-107">ResourceId</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="abb9f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="abb9f-108">DESCRIPTION</span></span>
<span data-ttu-id="abb9f-109">Mit den Einstellungen für die automatische Bereitstellung können Sie entscheiden, ob Azure Security Cetner einen Sicherheits-Agent automatisch proviosion soll, der auf ihren VMS installiert wird.</span><span class="sxs-lookup"><span data-stu-id="abb9f-109">Automatic Provisioning Settings let you decide whether you want Azure Security Cetner to automatically proviosion a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="abb9f-110">Der Security-Agent überwacht Ihre VM, um Sicherheitswarnungen zu erstellen und die Sicherheitskonformität des virtuellen Computers zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="abb9f-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="abb9f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="abb9f-111">EXAMPLES</span></span>

### <span data-ttu-id="abb9f-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="abb9f-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="abb9f-113">Ruft die Einstellung für die automatische Bereitstellung für das Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="abb9f-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="abb9f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="abb9f-114">PARAMETERS</span></span>

### <span data-ttu-id="abb9f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abb9f-115">-DefaultProfile</span></span>
<span data-ttu-id="abb9f-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="abb9f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abb9f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="abb9f-117">-Name</span></span>
<span data-ttu-id="abb9f-118">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="abb9f-118">Resource name.</span></span>

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

### <span data-ttu-id="abb9f-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="abb9f-119">-ResourceId</span></span>
<span data-ttu-id="abb9f-120">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="abb9f-120">Resource ID.</span></span>

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

### <span data-ttu-id="abb9f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abb9f-121">CommonParameters</span></span>
<span data-ttu-id="abb9f-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abb9f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abb9f-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abb9f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abb9f-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="abb9f-124">INPUTS</span></span>

### <span data-ttu-id="abb9f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="abb9f-125">System.String</span></span>

## <span data-ttu-id="abb9f-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="abb9f-126">OUTPUTS</span></span>

### <span data-ttu-id="abb9f-127">Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="abb9f-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="abb9f-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="abb9f-128">NOTES</span></span>

## <span data-ttu-id="abb9f-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="abb9f-129">RELATED LINKS</span></span>
