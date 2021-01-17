---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
ms.openlocfilehash: 7903e13abf7e924898910ad007eefcf6800dcc61
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473097"
---
# <span data-ttu-id="4c54c-101">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="4c54c-101">Get-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="4c54c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c54c-102">SYNOPSIS</span></span>
<span data-ttu-id="4c54c-103">Ruft die Einstellungen für eine SQL Server erweiterung auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="4c54c-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="4c54c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c54c-104">SYNTAX</span></span>

```
Get-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c54c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4c54c-105">DESCRIPTION</span></span>
<span data-ttu-id="4c54c-106">Das **Cmdlet "Get-AzVMSqlServerExtension"** ruft die Einstellungen der SQL Server-Infrastruktur als Dienst-Agent (IaaS)-Agent auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="4c54c-106">The **Get-AzVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="4c54c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4c54c-107">EXAMPLES</span></span>

### <span data-ttu-id="4c54c-108">Beispiel 1: Festlegen der Einstellungen für eine SQL Server auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="4c54c-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="4c54c-109">Dieser Befehl ruft die Einstellungen der Erweiterung SQL Server auf einem virtuellen Computer namens ContosoVM07 ab.</span><span class="sxs-lookup"><span data-stu-id="4c54c-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="4c54c-110">Beispiel 2: Erhalten der Einstellungen mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="4c54c-110">Example 2: Get the settings by using the pipeline</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service08" -Name "ContosoVM22" | Get-AzVMSqlServerExtension
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="4c54c-111">Dieser Befehl ruft den virtuellen Computer "ContosoVM22" im Dienst Service08 mithilfe des cmdlets Get-AzVM ab.</span><span class="sxs-lookup"><span data-stu-id="4c54c-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="4c54c-112">Der Befehl übergibt die Ergebnisse mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c54c-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4c54c-113">Der aktuelle Befehl ruft die Einstellungen des SQL Server A0 auf diesem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="4c54c-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="4c54c-114">Beispiel 3: Erhalten der Einstellungen für eine bestimmte SQL Server Version</span><span class="sxs-lookup"><span data-stu-id="4c54c-114">Example 3: Get the settings of specific SQL Server version</span></span>
```
PS C:\> Get-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07" -Version "1.0"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="4c54c-115">Dieser Befehl ruft die Einstellungen der Version 1.0 der SQL Server auf einem virtuellen Computer namens ContosoVM07 ab.</span><span class="sxs-lookup"><span data-stu-id="4c54c-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="4c54c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c54c-116">PARAMETERS</span></span>

### <span data-ttu-id="4c54c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c54c-117">-DefaultProfile</span></span>
<span data-ttu-id="4c54c-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c54c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c54c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4c54c-119">-Name</span></span>
<span data-ttu-id="4c54c-120">Gibt den Namen des Namens der SQL Server Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="4c54c-120">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c54c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c54c-121">-ResourceGroupName</span></span>
<span data-ttu-id="4c54c-122">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="4c54c-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="4c54c-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="4c54c-123">-VMName</span></span>
<span data-ttu-id="4c54c-124">Gibt den Namen des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="4c54c-124">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="4c54c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c54c-125">CommonParameters</span></span>
<span data-ttu-id="4c54c-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c54c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c54c-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c54c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c54c-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4c54c-128">INPUTS</span></span>

### <span data-ttu-id="4c54c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="4c54c-129">System.String</span></span>

## <span data-ttu-id="4c54c-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4c54c-130">OUTPUTS</span></span>

### <span data-ttu-id="4c54c-131">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span><span class="sxs-lookup"><span data-stu-id="4c54c-131">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span></span>

## <span data-ttu-id="4c54c-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4c54c-132">NOTES</span></span>

## <span data-ttu-id="4c54c-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4c54c-133">RELATED LINKS</span></span>

[<span data-ttu-id="4c54c-134">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="4c54c-134">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="4c54c-135">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="4c54c-135">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="4c54c-136">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="4c54c-136">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


