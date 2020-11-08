---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
ms.openlocfilehash: 58ae996e4d2723d4b38b548dd8225a2a483ce8f7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996163"
---
# <span data-ttu-id="a7647-101">New-AzHost</span><span class="sxs-lookup"><span data-stu-id="a7647-101">New-AzHost</span></span>

## <span data-ttu-id="a7647-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a7647-102">SYNOPSIS</span></span>
<span data-ttu-id="a7647-103">Erstellt einen Host.</span><span class="sxs-lookup"><span data-stu-id="a7647-103">Creates a  host.</span></span>

## <span data-ttu-id="a7647-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7647-104">SYNTAX</span></span>

```
New-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-Location] <String>
 -Sku <String> [-PlatformFaultDomain <Int32>] [-AutoReplaceOnFailure <Boolean>]
 [-LicenseType <DedicatedHostLicenseTypes>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7647-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7647-105">DESCRIPTION</span></span>
<span data-ttu-id="a7647-106">Mit diesem Cmdlet wird ein Host erstellt.</span><span class="sxs-lookup"><span data-stu-id="a7647-106">This cmdlet will create a Host.</span></span>

## <span data-ttu-id="a7647-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7647-107">EXAMPLES</span></span>

### <span data-ttu-id="a7647-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a7647-108">Example 1</span></span>
```
PS C:\> New-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName -Location $location -Sku $skuName

ResourceGroupName    : myrg01
PlatformFaultDomain  : 0
AutoReplaceOnFailure : True
HostId               : 00000000-0000-0000-0000-000000000000
ProvisioningTime     : 7/25/2019 8:34:16 PM
ProvisioningState    : Succeeded
Sku                  : 
  Name               : ESv3-Type1
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                 : myhost01
Location             : eastus
Tags                 : {"key1":"val2"}
```

<span data-ttu-id="a7647-109">Dieser Befehl erstellt einen Host der angegebenen SKU in der angegebenen Hostgruppe und der angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="a7647-109">This command creates a host of the given Sku in the given host group and the given location.</span></span>

## <span data-ttu-id="a7647-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7647-110">PARAMETERS</span></span>

### <span data-ttu-id="a7647-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7647-111">-AsJob</span></span>
<span data-ttu-id="a7647-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a7647-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7647-113">-AutoReplaceOnFailure</span><span class="sxs-lookup"><span data-stu-id="a7647-113">-AutoReplaceOnFailure</span></span>
<span data-ttu-id="a7647-114">Gibt an, ob der Host bei einem Fehler automatisch ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a7647-114">Specifies whether the host should be replaced automatically in case of a failure.</span></span> <span data-ttu-id="a7647-115">Der Wert wird standardmäßig auf "true" festgelegt, wenn er nicht bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a7647-115">The value is defaulted to 'true' when not provided.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7647-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7647-116">-DefaultProfile</span></span>
<span data-ttu-id="a7647-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a7647-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7647-118">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="a7647-118">-HostGroupName</span></span>
<span data-ttu-id="a7647-119">Gibt den Namen der Hostgruppe an.</span><span class="sxs-lookup"><span data-stu-id="a7647-119">Specifies the name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7647-120">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a7647-120">-LicenseType</span></span>
<span data-ttu-id="a7647-121">Gibt den Software-Lizenztyp an, der auf die VMs angewendet wird, die auf dem Host bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a7647-121">Specifies the software license type that will be applied to the VMs deployed on the host.</span></span> <span data-ttu-id="a7647-122">Mögliche Werte sind: None, Windows_Server_Hybrid und Windows_Server_Perpetual.</span><span class="sxs-lookup"><span data-stu-id="a7647-122">Possible values are: None, Windows_Server_Hybrid, and Windows_Server_Perpetual.</span></span>  <span data-ttu-id="a7647-123">Der Standardwert ist None.</span><span class="sxs-lookup"><span data-stu-id="a7647-123">Default value is None.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.DedicatedHostLicenseTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, WindowsServerHybrid, WindowsServerPerpetual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7647-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="a7647-124">-Location</span></span>
<span data-ttu-id="a7647-125">Gibt den Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="a7647-125">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7647-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a7647-126">-Name</span></span>
<span data-ttu-id="a7647-127">Gibt den Namen des Hosts an.</span><span class="sxs-lookup"><span data-stu-id="a7647-127">Specifies the name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7647-128">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="a7647-128">-PlatformFaultDomain</span></span>
<span data-ttu-id="a7647-129">Gibt die Anzahl der Plattform-fehlerdomäne des Hosts an.</span><span class="sxs-lookup"><span data-stu-id="a7647-129">Specifies the number of platform fault domain of the host.</span></span>  <span data-ttu-id="a7647-130">Dann ist der Mindestwert 0 und der Höchstwert 2.</span><span class="sxs-lookup"><span data-stu-id="a7647-130">Then minimum value is 0 and the maximum value is 2.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7647-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7647-131">-ResourceGroupName</span></span>
<span data-ttu-id="a7647-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a7647-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="a7647-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="a7647-133">-Sku</span></span>
<span data-ttu-id="a7647-134">Gibt den Namen der SKU an.</span><span class="sxs-lookup"><span data-stu-id="a7647-134">Specifies the name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7647-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="a7647-135">-Tag</span></span>
<span data-ttu-id="a7647-136">Gibt Tags an.</span><span class="sxs-lookup"><span data-stu-id="a7647-136">Specifies Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7647-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a7647-137">-Confirm</span></span>
<span data-ttu-id="a7647-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a7647-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7647-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7647-139">-WhatIf</span></span>
<span data-ttu-id="a7647-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a7647-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7647-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7647-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7647-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7647-142">CommonParameters</span></span>
<span data-ttu-id="a7647-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7647-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7647-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7647-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7647-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a7647-145">INPUTS</span></span>

### <span data-ttu-id="a7647-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a7647-146">System.String</span></span>

## <span data-ttu-id="a7647-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a7647-147">OUTPUTS</span></span>

### <span data-ttu-id="a7647-148">Microsoft. Azure. Commands. Compute. Automation. Models. PSHost</span><span class="sxs-lookup"><span data-stu-id="a7647-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="a7647-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="a7647-149">NOTES</span></span>

## <span data-ttu-id="a7647-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a7647-150">RELATED LINKS</span></span>
