---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 399a4c8a400f9835aba15fc7ad0448430854e467
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662776"
---
# <span data-ttu-id="250d4-101">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="250d4-101">Get-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="250d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="250d4-102">SYNOPSIS</span></span>
<span data-ttu-id="250d4-103">Ruft eine Netzwerksicherheitsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="250d4-103">Gets a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="250d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="250d4-104">SYNTAX</span></span>

### <span data-ttu-id="250d4-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="250d4-105">NoExpand</span></span>
```
Get-AzureRmNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="250d4-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="250d4-106">Expand</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="250d4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="250d4-107">DESCRIPTION</span></span>
<span data-ttu-id="250d4-108">Das Cmdlet " **Get-AzureRmNetworkSecurityGroup** " Ruft eine Azure Network Security-Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="250d4-108">The **Get-AzureRmNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="250d4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="250d4-109">EXAMPLES</span></span>

### <span data-ttu-id="250d4-110">1: Abrufen einer vorhandenen Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="250d4-110">1: Retrieve an existing network security group</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="250d4-111">Dieser Befehl gibt den Inhalt der Azure Network Security-Gruppe "nsg1" in der Ressourcengruppe "RG1" zurück.</span><span class="sxs-lookup"><span data-stu-id="250d4-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="250d4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="250d4-112">PARAMETERS</span></span>

### <span data-ttu-id="250d4-113">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="250d4-113">-ExpandResource</span></span>
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

### <span data-ttu-id="250d4-114">-Name</span><span class="sxs-lookup"><span data-stu-id="250d4-114">-Name</span></span>
<span data-ttu-id="250d4-115">Gibt den Namen der Netzwerksicherheitsgruppe an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="250d4-115">Specifies the name of the network security group that this cmdlet gets.</span></span>

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

### <span data-ttu-id="250d4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="250d4-116">-ResourceGroupName</span></span>
<span data-ttu-id="250d4-117">Gibt den Namen der Ressourcengruppe an, zu der die Netzwerksicherheitsgruppe gehört.</span><span class="sxs-lookup"><span data-stu-id="250d4-117">Specifies the name of the resource group that the network security group belongs to.</span></span>

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

### <span data-ttu-id="250d4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="250d4-118">-DefaultProfile</span></span>
<span data-ttu-id="250d4-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="250d4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="250d4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="250d4-120">CommonParameters</span></span>
<span data-ttu-id="250d4-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="250d4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="250d4-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="250d4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="250d4-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="250d4-123">INPUTS</span></span>

## <span data-ttu-id="250d4-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="250d4-124">OUTPUTS</span></span>

### <span data-ttu-id="250d4-125">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="250d4-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="250d4-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="250d4-126">NOTES</span></span>

## <span data-ttu-id="250d4-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="250d4-127">RELATED LINKS</span></span>

[<span data-ttu-id="250d4-128">Neu – AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="250d4-128">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="250d4-129">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="250d4-129">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="250d4-130">Satz-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="250d4-130">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


