---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8CDB4C0A-A050-4F65-8CC0-1822D006D772
online version: ''
schema: 2.0.0
ms.openlocfilehash: eb0fe27a664badd5f32b941e80b2c8e2cba2d2a4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006075"
---
# <span data-ttu-id="9fb92-101">Remove-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="9fb92-101">Remove-AzureNetworkSecurityRule</span></span>

## <span data-ttu-id="9fb92-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9fb92-102">SYNOPSIS</span></span>
<span data-ttu-id="9fb92-103">Entfernt eine Netzwerk Sicherheitsregel aus einer Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9fb92-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="9fb92-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fb92-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityRule -Name <String> [-Force] -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9fb92-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9fb92-105">DESCRIPTION</span></span>
<span data-ttu-id="9fb92-106">Das Cmdlet **Remove-AzureNetworkSecurityRule** entfernt eine Azure Network Security-Regel aus einer Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9fb92-106">The **Remove-AzureNetworkSecurityRule** cmdlet removes an Azure network security rule from a network security group.</span></span>

## <span data-ttu-id="9fb92-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9fb92-107">EXAMPLES</span></span>

## <span data-ttu-id="9fb92-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fb92-108">PARAMETERS</span></span>

### <span data-ttu-id="9fb92-109">-Force</span><span class="sxs-lookup"><span data-stu-id="9fb92-109">-Force</span></span>
<span data-ttu-id="9fb92-110">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="9fb92-110">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb92-111">-Name</span><span class="sxs-lookup"><span data-stu-id="9fb92-111">-Name</span></span>
<span data-ttu-id="9fb92-112">Gibt den Namen der Netzwerk Sicherheitsregel an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="9fb92-112">Specifies the name for the network security rule that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb92-113">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9fb92-113">-NetworkSecurityGroup</span></span>
<span data-ttu-id="9fb92-114">Gibt die Netzwerksicherheitsgruppe an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9fb92-114">Specifies the network security group that this cmdlet modifies.</span></span>
<span data-ttu-id="9fb92-115">Verwenden Sie das Get-AzureNetworkSecurityGroup-Cmdlet, um ein **INetworkSecurityGroup** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9fb92-115">To obtain an **INetworkSecurityGroup** object, use the Get-AzureNetworkSecurityGroup cmdlet.</span></span>

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb92-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="9fb92-116">-Profile</span></span>
<span data-ttu-id="9fb92-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="9fb92-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9fb92-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="9fb92-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb92-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fb92-119">CommonParameters</span></span>
<span data-ttu-id="9fb92-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fb92-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fb92-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fb92-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fb92-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9fb92-122">INPUTS</span></span>

## <span data-ttu-id="9fb92-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9fb92-123">OUTPUTS</span></span>

## <span data-ttu-id="9fb92-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="9fb92-124">NOTES</span></span>

## <span data-ttu-id="9fb92-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9fb92-125">RELATED LINKS</span></span>

[<span data-ttu-id="9fb92-126">Satz-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="9fb92-126">Set-AzureNetworkSecurityRule</span></span>](./Set-AzureNetworkSecurityRule.md)


