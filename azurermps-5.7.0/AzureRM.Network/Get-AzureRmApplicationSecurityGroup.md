---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 5a1c519bd545ecb750f3842dac490eb31703e4d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663225"
---
# <span data-ttu-id="30612-101">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="30612-101">Get-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="30612-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="30612-102">SYNOPSIS</span></span>
<span data-ttu-id="30612-103">Ruft eine Anwendungs Sicherheitsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="30612-103">Gets an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30612-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="30612-104">SYNTAX</span></span>

```
Get-AzureRmApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30612-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30612-105">DESCRIPTION</span></span>
<span data-ttu-id="30612-106">Das Cmdlet " **Get-AzureRmApplicationSecurityGroup** " Ruft eine Anwendungs Sicherheitsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="30612-106">The **Get-AzureRmApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="30612-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="30612-107">EXAMPLES</span></span>

### <span data-ttu-id="30612-108">Beispiel 1: Abrufen aller Anwendungs Sicherheitsgruppen</span><span class="sxs-lookup"><span data-stu-id="30612-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup
```

<span data-ttu-id="30612-109">Der obige Befehl gibt alle Anwendungs Sicherheitsgruppen im Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="30612-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="30612-110">Beispiel 2: Abrufen von Anwendungs Sicherheitsgruppen in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="30612-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="30612-111">Der obige Befehl gibt alle Anwendungs Sicherheitsgruppen zurück, die zur Ressourcengruppe myresourcegroup gehören.</span><span class="sxs-lookup"><span data-stu-id="30612-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="30612-112">Beispiel 3: Abrufen einer bestimmten Anwendungs Sicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="30612-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

<span data-ttu-id="30612-113">Der obige Befehl gibt die Anwendungs Sicherheitsgruppe MyApplicationSecurityGroup unter der Ressourcengruppe myresourcegroup zurück.</span><span class="sxs-lookup"><span data-stu-id="30612-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

## <span data-ttu-id="30612-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="30612-114">PARAMETERS</span></span>

### <span data-ttu-id="30612-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30612-115">-DefaultProfile</span></span>
<span data-ttu-id="30612-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="30612-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30612-117">-Name</span><span class="sxs-lookup"><span data-stu-id="30612-117">-Name</span></span>
<span data-ttu-id="30612-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="30612-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30612-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30612-119">-ResourceGroupName</span></span>
<span data-ttu-id="30612-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="30612-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30612-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30612-121">CommonParameters</span></span>
<span data-ttu-id="30612-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30612-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30612-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30612-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30612-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="30612-124">INPUTS</span></span>

### <span data-ttu-id="30612-125">System. String</span><span class="sxs-lookup"><span data-stu-id="30612-125">System.String</span></span>

## <span data-ttu-id="30612-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="30612-126">OUTPUTS</span></span>

### <span data-ttu-id="30612-127">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="30612-127">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="30612-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="30612-128">NOTES</span></span>

## <span data-ttu-id="30612-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="30612-129">RELATED LINKS</span></span>

[<span data-ttu-id="30612-130">Neu – AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="30612-130">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="30612-131">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="30612-131">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="30612-132">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30612-132">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="30612-133">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="30612-133">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)
