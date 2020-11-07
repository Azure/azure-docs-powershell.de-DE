---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
ms.openlocfilehash: beb2b723a0b72f7ab485846f6f55fabd4e6ef9aa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841600"
---
# <span data-ttu-id="70fd4-101">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="70fd4-101">Get-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="70fd4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="70fd4-102">SYNOPSIS</span></span>
<span data-ttu-id="70fd4-103">Ruft eine Netzwerksicherheitsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="70fd4-103">Gets a network security group.</span></span>

## <span data-ttu-id="70fd4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="70fd4-104">SYNTAX</span></span>

### <span data-ttu-id="70fd4-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="70fd4-105">NoExpand</span></span>
```
Get-AzNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70fd4-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="70fd4-106">Expand</span></span>
```
Get-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70fd4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70fd4-107">DESCRIPTION</span></span>
<span data-ttu-id="70fd4-108">Das Cmdlet " **Get-AzNetworkSecurityGroup** " Ruft eine Azure Network Security-Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="70fd4-108">The **Get-AzNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="70fd4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70fd4-109">EXAMPLES</span></span>

### <span data-ttu-id="70fd4-110">1: Abrufen einer vorhandenen Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="70fd4-110">1: Retrieve an existing network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="70fd4-111">Dieser Befehl gibt den Inhalt der Azure Network Security-Gruppe "nsg1" in der Ressourcengruppe "RG1" zurück.</span><span class="sxs-lookup"><span data-stu-id="70fd4-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="70fd4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="70fd4-112">PARAMETERS</span></span>

### <span data-ttu-id="70fd4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70fd4-113">-DefaultProfile</span></span>
<span data-ttu-id="70fd4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="70fd4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70fd4-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="70fd4-115">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70fd4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="70fd4-116">-Name</span></span>
<span data-ttu-id="70fd4-117">Gibt den Namen der Netzwerksicherheitsgruppe an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="70fd4-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70fd4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70fd4-118">-ResourceGroupName</span></span>
<span data-ttu-id="70fd4-119">Gibt den Namen der Ressourcengruppe an, zu der die Netzwerksicherheitsgruppe gehört.</span><span class="sxs-lookup"><span data-stu-id="70fd4-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70fd4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70fd4-120">CommonParameters</span></span>
<span data-ttu-id="70fd4-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70fd4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70fd4-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70fd4-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70fd4-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="70fd4-123">INPUTS</span></span>

## <span data-ttu-id="70fd4-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="70fd4-124">OUTPUTS</span></span>

### <span data-ttu-id="70fd4-125">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="70fd4-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="70fd4-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="70fd4-126">NOTES</span></span>

## <span data-ttu-id="70fd4-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="70fd4-127">RELATED LINKS</span></span>

[<span data-ttu-id="70fd4-128">Neu – AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="70fd4-128">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="70fd4-129">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="70fd4-129">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="70fd4-130">Satz-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="70fd4-130">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


