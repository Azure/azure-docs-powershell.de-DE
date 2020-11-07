---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 955c5200b7c7b9716e096f1157f7179619ae4f5c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848411"
---
# <span data-ttu-id="ead89-101">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ead89-101">Remove-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="ead89-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ead89-102">SYNOPSIS</span></span>
<span data-ttu-id="ead89-103">Entfernt eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ead89-103">Removes a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ead89-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ead89-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ead89-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ead89-105">DESCRIPTION</span></span>
<span data-ttu-id="ead89-106">Das Cmdlet **Remove-AzureRmNetworkInterface** entfernt eine Azure-Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ead89-106">The **Remove-AzureRmNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="ead89-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ead89-107">EXAMPLES</span></span>

### <span data-ttu-id="ead89-108">Beispiel 1: Entfernen einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="ead89-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="ead89-109">Dieser Befehl entfernt die Netzwerkschnittstellen-NetworkInterface1 in der Ressourcengruppe ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="ead89-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="ead89-110">Da der Parameter *Force* nicht verwendet wird, wird der Benutzer aufgefordert, diese Aktion zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="ead89-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="ead89-111">Beispiel 2: Entfernen einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="ead89-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzureRmNetworkInterface -Force
```

<span data-ttu-id="ead89-112">Dieser Befehl entfernt alle Netzwerkschnittstellen in der Ressourcengruppe ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="ead89-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="ead89-113">Da der Parameter *Force* verwendet wird, wird der Benutzer nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="ead89-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="ead89-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ead89-114">PARAMETERS</span></span>

### <span data-ttu-id="ead89-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ead89-115">-AsJob</span></span>
<span data-ttu-id="ead89-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ead89-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ead89-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ead89-117">-DefaultProfile</span></span>
<span data-ttu-id="ead89-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ead89-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ead89-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ead89-119">-Force</span></span>
<span data-ttu-id="ead89-120">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="ead89-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ead89-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ead89-121">-Name</span></span>
<span data-ttu-id="ead89-122">Gibt den Namen der Netzwerkschnittstelle an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="ead89-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ead89-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ead89-123">-PassThru</span></span>
<span data-ttu-id="ead89-124">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ead89-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ead89-125">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="ead89-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ead89-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ead89-126">-ResourceGroupName</span></span>
<span data-ttu-id="ead89-127">Gibt den Namen einer Ressourcengruppe an, die die vom Cmdlet entfernte Netzwerkschnittstelle enthält.</span><span class="sxs-lookup"><span data-stu-id="ead89-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ead89-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ead89-128">-Confirm</span></span>
<span data-ttu-id="ead89-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ead89-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ead89-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ead89-130">-WhatIf</span></span>
<span data-ttu-id="ead89-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ead89-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ead89-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ead89-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ead89-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ead89-133">CommonParameters</span></span>
<span data-ttu-id="ead89-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ead89-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ead89-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ead89-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ead89-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ead89-136">INPUTS</span></span>

## <span data-ttu-id="ead89-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ead89-137">OUTPUTS</span></span>

## <span data-ttu-id="ead89-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="ead89-138">NOTES</span></span>

## <span data-ttu-id="ead89-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ead89-139">RELATED LINKS</span></span>

[<span data-ttu-id="ead89-140">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ead89-140">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="ead89-141">Neu – AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ead89-141">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="ead89-142">Satz-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ead89-142">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


