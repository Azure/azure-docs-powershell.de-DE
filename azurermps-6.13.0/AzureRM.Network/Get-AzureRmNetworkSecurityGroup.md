---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 32bcc3b83ad34a0f60b01048212d402745934317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505753"
---
# <span data-ttu-id="43159-101">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="43159-101">Get-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="43159-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43159-102">SYNOPSIS</span></span>
<span data-ttu-id="43159-103">Ruft eine Netzwerksicherheitsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="43159-103">Gets a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43159-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43159-104">SYNTAX</span></span>

### <span data-ttu-id="43159-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="43159-105">NoExpand</span></span>
```
Get-AzureRmNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43159-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="43159-106">Expand</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43159-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43159-107">DESCRIPTION</span></span>
<span data-ttu-id="43159-108">Das Cmdlet " **Get-AzureRmNetworkSecurityGroup** " Ruft eine Azure Network Security-Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="43159-108">The **Get-AzureRmNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="43159-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43159-109">EXAMPLES</span></span>

### <span data-ttu-id="43159-110">1: Abrufen einer vorhandenen Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="43159-110">1: Retrieve an existing network security group</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="43159-111">Dieser Befehl gibt den Inhalt der Azure Network Security-Gruppe "nsg1" in der Ressourcengruppe "RG1" zurück.</span><span class="sxs-lookup"><span data-stu-id="43159-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="43159-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="43159-112">PARAMETERS</span></span>

### <span data-ttu-id="43159-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43159-113">-DefaultProfile</span></span>
<span data-ttu-id="43159-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="43159-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43159-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="43159-115">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43159-116">-Name</span><span class="sxs-lookup"><span data-stu-id="43159-116">-Name</span></span>
<span data-ttu-id="43159-117">Gibt den Namen der Netzwerksicherheitsgruppe an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="43159-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43159-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43159-118">-ResourceGroupName</span></span>
<span data-ttu-id="43159-119">Gibt den Namen der Ressourcengruppe an, zu der die Netzwerksicherheitsgruppe gehört.</span><span class="sxs-lookup"><span data-stu-id="43159-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43159-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43159-120">CommonParameters</span></span>
<span data-ttu-id="43159-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43159-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43159-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43159-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43159-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43159-123">INPUTS</span></span>

### <span data-ttu-id="43159-124">System. String</span><span class="sxs-lookup"><span data-stu-id="43159-124">System.String</span></span>

## <span data-ttu-id="43159-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43159-125">OUTPUTS</span></span>

### <span data-ttu-id="43159-126">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="43159-126">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="43159-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="43159-127">NOTES</span></span>

## <span data-ttu-id="43159-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43159-128">RELATED LINKS</span></span>

[<span data-ttu-id="43159-129">Neu – AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="43159-129">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="43159-130">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="43159-130">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="43159-131">Satz-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="43159-131">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


