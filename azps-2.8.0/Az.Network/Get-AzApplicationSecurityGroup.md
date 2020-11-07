---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: 58bae669af1fb9a06f4caa95070225f12d1a78aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821899"
---
# <span data-ttu-id="573ba-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="573ba-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="573ba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="573ba-102">SYNOPSIS</span></span>
<span data-ttu-id="573ba-103">Ruft eine Anwendungs Sicherheitsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="573ba-103">Gets an application security group.</span></span>

## <span data-ttu-id="573ba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="573ba-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="573ba-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="573ba-105">DESCRIPTION</span></span>
<span data-ttu-id="573ba-106">Das Cmdlet " **Get-AzApplicationSecurityGroup** " Ruft eine Anwendungs Sicherheitsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="573ba-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="573ba-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="573ba-107">EXAMPLES</span></span>

### <span data-ttu-id="573ba-108">Beispiel 1: Abrufen aller Anwendungs Sicherheitsgruppen</span><span class="sxs-lookup"><span data-stu-id="573ba-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="573ba-109">Der obige Befehl gibt alle Anwendungs Sicherheitsgruppen im Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="573ba-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="573ba-110">Beispiel 2: Abrufen von Anwendungs Sicherheitsgruppen in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="573ba-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="573ba-111">Der obige Befehl gibt alle Anwendungs Sicherheitsgruppen zurück, die zur Ressourcengruppe myresourcegroup gehören.</span><span class="sxs-lookup"><span data-stu-id="573ba-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="573ba-112">Beispiel 3: Abrufen einer bestimmten Anwendungs Sicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="573ba-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1
```

<span data-ttu-id="573ba-113">Der obige Befehl gibt die Anwendungs Sicherheitsgruppe MyApplicationSecurityGroup unter der Ressourcengruppe myresourcegroup zurück.</span><span class="sxs-lookup"><span data-stu-id="573ba-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="573ba-114">Beispiel 4: Abrufen von Anwendungs Sicherheitsgruppen mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="573ba-114">Example 4: Retrieve application security groups using filtering.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -Name MyApplicationSecurityGroup*

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="573ba-115">Der obige Befehl gibt alle Anwendungs Sicherheitsgruppen zurück, die mit "MyApplicationSecurityGroup" beginnen.</span><span class="sxs-lookup"><span data-stu-id="573ba-115">The command above returns all application security groups that start with "MyApplicationSecurityGroup".</span></span>

## <span data-ttu-id="573ba-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="573ba-116">PARAMETERS</span></span>

### <span data-ttu-id="573ba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="573ba-117">-DefaultProfile</span></span>
<span data-ttu-id="573ba-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="573ba-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="573ba-119">-Name</span><span class="sxs-lookup"><span data-stu-id="573ba-119">-Name</span></span>
<span data-ttu-id="573ba-120">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="573ba-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="573ba-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="573ba-121">-ResourceGroupName</span></span>
<span data-ttu-id="573ba-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="573ba-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="573ba-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="573ba-123">CommonParameters</span></span>
<span data-ttu-id="573ba-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="573ba-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="573ba-125">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="573ba-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="573ba-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="573ba-126">INPUTS</span></span>

### <span data-ttu-id="573ba-127">System. String</span><span class="sxs-lookup"><span data-stu-id="573ba-127">System.String</span></span>

## <span data-ttu-id="573ba-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="573ba-128">OUTPUTS</span></span>

### <span data-ttu-id="573ba-129">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="573ba-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="573ba-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="573ba-130">NOTES</span></span>

## <span data-ttu-id="573ba-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="573ba-131">RELATED LINKS</span></span>

[<span data-ttu-id="573ba-132">Neu – AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="573ba-132">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="573ba-133">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="573ba-133">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="573ba-134">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="573ba-134">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="573ba-135">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="573ba-135">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)
