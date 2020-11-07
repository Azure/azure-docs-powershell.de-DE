---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: b23901a79262f4eb63e34b99c10b82442cb2fe6a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841684"
---
# <span data-ttu-id="29f11-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="29f11-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="29f11-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29f11-102">SYNOPSIS</span></span>
<span data-ttu-id="29f11-103">Ruft eine Anwendungs Sicherheitsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="29f11-103">Gets an application security group.</span></span>

## <span data-ttu-id="29f11-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29f11-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29f11-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29f11-105">DESCRIPTION</span></span>
<span data-ttu-id="29f11-106">Das Cmdlet " **Get-AzApplicationSecurityGroup** " Ruft eine Anwendungs Sicherheitsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="29f11-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="29f11-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29f11-107">EXAMPLES</span></span>

### <span data-ttu-id="29f11-108">Beispiel 1: Abrufen aller Anwendungs Sicherheitsgruppen</span><span class="sxs-lookup"><span data-stu-id="29f11-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup
```

<span data-ttu-id="29f11-109">Der obige Befehl gibt alle Anwendungs Sicherheitsgruppen im Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="29f11-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="29f11-110">Beispiel 2: Abrufen von Anwendungs Sicherheitsgruppen in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="29f11-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="29f11-111">Der obige Befehl gibt alle Anwendungs Sicherheitsgruppen zurück, die zur Ressourcengruppe myresourcegroup gehören.</span><span class="sxs-lookup"><span data-stu-id="29f11-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="29f11-112">Beispiel 3: Abrufen einer bestimmten Anwendungs Sicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="29f11-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

<span data-ttu-id="29f11-113">Der obige Befehl gibt die Anwendungs Sicherheitsgruppe MyApplicationSecurityGroup unter der Ressourcengruppe myresourcegroup zurück.</span><span class="sxs-lookup"><span data-stu-id="29f11-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

## <span data-ttu-id="29f11-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="29f11-114">PARAMETERS</span></span>

### <span data-ttu-id="29f11-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29f11-115">-DefaultProfile</span></span>
<span data-ttu-id="29f11-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="29f11-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29f11-117">-Name</span><span class="sxs-lookup"><span data-stu-id="29f11-117">-Name</span></span>
<span data-ttu-id="29f11-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="29f11-118">The resource name.</span></span>

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

### <span data-ttu-id="29f11-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29f11-119">-ResourceGroupName</span></span>
<span data-ttu-id="29f11-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="29f11-120">The resource group name.</span></span>

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

### <span data-ttu-id="29f11-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29f11-121">CommonParameters</span></span>
<span data-ttu-id="29f11-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29f11-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29f11-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29f11-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29f11-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29f11-124">INPUTS</span></span>

### <span data-ttu-id="29f11-125">System. String</span><span class="sxs-lookup"><span data-stu-id="29f11-125">System.String</span></span>

## <span data-ttu-id="29f11-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29f11-126">OUTPUTS</span></span>

### <span data-ttu-id="29f11-127">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="29f11-127">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="29f11-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="29f11-128">NOTES</span></span>

## <span data-ttu-id="29f11-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29f11-129">RELATED LINKS</span></span>

[<span data-ttu-id="29f11-130">Neu – AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="29f11-130">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="29f11-131">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="29f11-131">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="29f11-132">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="29f11-132">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="29f11-133">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="29f11-133">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)
