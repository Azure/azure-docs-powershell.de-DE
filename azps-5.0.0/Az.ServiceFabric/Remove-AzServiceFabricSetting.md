---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
ms.openlocfilehash: db6d94b4aa2f6182abc114f11d1dba0b40ebbb93
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176061"
---
# <span data-ttu-id="367b8-101">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="367b8-101">Remove-AzServiceFabricSetting</span></span>

## <span data-ttu-id="367b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="367b8-102">SYNOPSIS</span></span>
<span data-ttu-id="367b8-103">Entfernen einer oder mehrerer Service Fabric-Einstellungen aus dem Cluster</span><span class="sxs-lookup"><span data-stu-id="367b8-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

## <span data-ttu-id="367b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="367b8-104">SYNTAX</span></span>

### <span data-ttu-id="367b8-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="367b8-105">OneSetting</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="367b8-106">Batch Einstellungen</span><span class="sxs-lookup"><span data-stu-id="367b8-106">BatchSettings</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="367b8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="367b8-107">DESCRIPTION</span></span>
<span data-ttu-id="367b8-108">Verwenden **Sie Remove-AzServiceFabricSetting** , um die Service Fabric-Einstellungen aus dem Cluster zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="367b8-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="367b8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="367b8-109">EXAMPLES</span></span>

### <span data-ttu-id="367b8-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="367b8-110">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="367b8-111">Dieser Befehl entfernt die Einstellungen "MaxCursors" unter "EseStore".</span><span class="sxs-lookup"><span data-stu-id="367b8-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="367b8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="367b8-112">PARAMETERS</span></span>

### <span data-ttu-id="367b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="367b8-113">-DefaultProfile</span></span>
<span data-ttu-id="367b8-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="367b8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="367b8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="367b8-115">-Name</span></span>
<span data-ttu-id="367b8-116">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="367b8-116">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="367b8-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="367b8-117">-Parameter</span></span>
<span data-ttu-id="367b8-118">Parameter Name der Fabric-Einstellung</span><span class="sxs-lookup"><span data-stu-id="367b8-118">Parameter name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="367b8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="367b8-119">-ResourceGroupName</span></span>
<span data-ttu-id="367b8-120">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="367b8-120">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="367b8-121">-Section</span><span class="sxs-lookup"><span data-stu-id="367b8-121">-Section</span></span>
<span data-ttu-id="367b8-122">Abschnittsname der Fabric-Einstellung</span><span class="sxs-lookup"><span data-stu-id="367b8-122">Section name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="367b8-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="367b8-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="367b8-124">Ein Array von Fabric-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="367b8-124">An array of fabric settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="367b8-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="367b8-125">-Confirm</span></span>
<span data-ttu-id="367b8-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="367b8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="367b8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="367b8-127">-WhatIf</span></span>
<span data-ttu-id="367b8-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="367b8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="367b8-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="367b8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="367b8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="367b8-130">CommonParameters</span></span>
<span data-ttu-id="367b8-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="367b8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="367b8-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="367b8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="367b8-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="367b8-133">INPUTS</span></span>

### <span data-ttu-id="367b8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="367b8-134">System.String</span></span>

### <span data-ttu-id="367b8-135">Microsoft. Azure. Commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="367b8-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="367b8-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="367b8-136">OUTPUTS</span></span>

### <span data-ttu-id="367b8-137">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="367b8-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="367b8-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="367b8-138">NOTES</span></span>

## <span data-ttu-id="367b8-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="367b8-139">RELATED LINKS</span></span>
