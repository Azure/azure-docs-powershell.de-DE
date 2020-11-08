---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
ms.openlocfilehash: edbfdcdfc7e02c8bfdb266e1ec7a6b1308c07fa2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165126"
---
# <span data-ttu-id="188ca-101">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="188ca-101">Set-AzNetworkProfile</span></span>

## <span data-ttu-id="188ca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="188ca-102">SYNOPSIS</span></span>
<span data-ttu-id="188ca-103">Aktualisiert ein Netzwerkprofil.</span><span class="sxs-lookup"><span data-stu-id="188ca-103">Updates a network profile.</span></span>

## <span data-ttu-id="188ca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="188ca-104">SYNTAX</span></span>

```
Set-AzNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="188ca-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="188ca-105">DESCRIPTION</span></span>
<span data-ttu-id="188ca-106">Das Cmdlet " **Satz-AzPublicIpPrefix** " aktualisiert ein Netzwerkprofil.</span><span class="sxs-lookup"><span data-stu-id="188ca-106">The **Set-AzPublicIpPrefix** cmdlet updates a network profile.</span></span>

## <span data-ttu-id="188ca-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="188ca-107">EXAMPLES</span></span>

### <span data-ttu-id="188ca-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="188ca-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzNetworkProfile
```

<span data-ttu-id="188ca-109">Der erste Befehl ruft ein vorhandenes Netzwerkprofil ab.</span><span class="sxs-lookup"><span data-stu-id="188ca-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="188ca-110">Der zweite Befehl aktualisiert eine Kategorie, und die dritte fügt eine Netzwerkschnittstellenkonfiguration für das Netzwerkprofil hinzu.</span><span class="sxs-lookup"><span data-stu-id="188ca-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="188ca-111">Der vierte Befehl aktualisiert das Netzwerkprofil.</span><span class="sxs-lookup"><span data-stu-id="188ca-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="188ca-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="188ca-112">PARAMETERS</span></span>

### <span data-ttu-id="188ca-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="188ca-113">-AsJob</span></span>
<span data-ttu-id="188ca-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="188ca-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="188ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="188ca-115">-DefaultProfile</span></span>
<span data-ttu-id="188ca-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="188ca-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="188ca-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="188ca-117">-NetworkProfile</span></span>
<span data-ttu-id="188ca-118">Das Netzwerkprofil</span><span class="sxs-lookup"><span data-stu-id="188ca-118">The network profile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="188ca-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="188ca-119">-Confirm</span></span>
<span data-ttu-id="188ca-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="188ca-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="188ca-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="188ca-121">-WhatIf</span></span>
<span data-ttu-id="188ca-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="188ca-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="188ca-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="188ca-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="188ca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="188ca-124">CommonParameters</span></span>
<span data-ttu-id="188ca-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="188ca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="188ca-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="188ca-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="188ca-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="188ca-127">INPUTS</span></span>

### <span data-ttu-id="188ca-128">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="188ca-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="188ca-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="188ca-129">OUTPUTS</span></span>

### <span data-ttu-id="188ca-130">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="188ca-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="188ca-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="188ca-131">NOTES</span></span>

## <span data-ttu-id="188ca-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="188ca-132">RELATED LINKS</span></span>

[<span data-ttu-id="188ca-133">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="188ca-133">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="188ca-134">Neu – AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="188ca-134">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="188ca-135">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="188ca-135">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)
