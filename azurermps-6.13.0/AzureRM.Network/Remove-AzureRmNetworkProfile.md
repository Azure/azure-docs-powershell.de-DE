---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkProfile.md
ms.openlocfilehash: ebf2a58530f1dabe0e320dd78a38c63c86565c73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664542"
---
# <span data-ttu-id="2aa4f-101">Remove-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2aa4f-101">Remove-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="2aa4f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2aa4f-102">SYNOPSIS</span></span>
<span data-ttu-id="2aa4f-103">Entfernt ein Netzwerkprofil.</span><span class="sxs-lookup"><span data-stu-id="2aa4f-103">Removes a network profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2aa4f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2aa4f-104">SYNTAX</span></span>

### <span data-ttu-id="2aa4f-105">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="2aa4f-105">RemoveByName</span></span>
```
Remove-AzureRmNetworkProfile -ResourceGroupName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aa4f-106">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2aa4f-106">RemoveByNameParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aa4f-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2aa4f-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aa4f-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2aa4f-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2aa4f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2aa4f-109">DESCRIPTION</span></span>
<span data-ttu-id="2aa4f-110">Das Cmdlet **Remove-AzureRmNetworkProfile** entfernt ein Netzwerkprofil, wenn keine Container Netzwerkschnittstellen (im Gegensatz zu einer Container-Netzwerkschnittstellen **Konfiguration** ) erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="2aa4f-110">The **Remove-AzureRmNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration** ) have been created.</span></span>

## <span data-ttu-id="2aa4f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2aa4f-111">EXAMPLES</span></span>

### <span data-ttu-id="2aa4f-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2aa4f-112">Example 1</span></span>
```powershell
Remove-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="2aa4f-113">Dadurch wird das Netzwerkprofil mit dem Namen Np1 aus der Ressourcengruppe RG1 entfernt.</span><span class="sxs-lookup"><span data-stu-id="2aa4f-113">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="2aa4f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2aa4f-114">PARAMETERS</span></span>

### <span data-ttu-id="2aa4f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2aa4f-115">-AsJob</span></span>
<span data-ttu-id="2aa4f-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2aa4f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2aa4f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aa4f-117">-DefaultProfile</span></span>
<span data-ttu-id="2aa4f-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2aa4f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2aa4f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2aa4f-119">-Force</span></span>
<span data-ttu-id="2aa4f-120">Keine Bestätigung anfordern, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="2aa4f-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="2aa4f-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2aa4f-121">-InputObject</span></span>
<span data-ttu-id="2aa4f-122">Netzwerkprofil Objekt.</span><span class="sxs-lookup"><span data-stu-id="2aa4f-122">Network profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa4f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2aa4f-123">-Name</span></span>
<span data-ttu-id="2aa4f-124">Der Name des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="2aa4f-124">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa4f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2aa4f-125">-PassThru</span></span>
<span data-ttu-id="2aa4f-126">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="2aa4f-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2aa4f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aa4f-127">-ResourceGroupName</span></span>
<span data-ttu-id="2aa4f-128">Der Ressourcengruppenname des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="2aa4f-128">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa4f-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2aa4f-129">-ResourceId</span></span>
<span data-ttu-id="2aa4f-130">Die Azure Resource Manager-Ressourcen-ID des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="2aa4f-130">The Azure resource manager resource ID of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa4f-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2aa4f-131">-Confirm</span></span>
<span data-ttu-id="2aa4f-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2aa4f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2aa4f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2aa4f-133">-WhatIf</span></span>
<span data-ttu-id="2aa4f-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2aa4f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2aa4f-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2aa4f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2aa4f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aa4f-136">CommonParameters</span></span>
<span data-ttu-id="2aa4f-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aa4f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aa4f-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aa4f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aa4f-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2aa4f-139">INPUTS</span></span>

### <span data-ttu-id="2aa4f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2aa4f-140">System.String</span></span>

## <span data-ttu-id="2aa4f-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2aa4f-141">OUTPUTS</span></span>

### <span data-ttu-id="2aa4f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2aa4f-142">System.Boolean</span></span>

## <span data-ttu-id="2aa4f-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="2aa4f-143">NOTES</span></span>

## <span data-ttu-id="2aa4f-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2aa4f-144">RELATED LINKS</span></span>
