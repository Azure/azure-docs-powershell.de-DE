---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
ms.openlocfilehash: 7903e13abf7e924898910ad007eefcf6800dcc61
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175821"
---
# <span data-ttu-id="b9f81-101">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b9f81-101">Get-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="b9f81-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b9f81-102">SYNOPSIS</span></span>
<span data-ttu-id="b9f81-103">Ruft die Einstellungen für eine SQL Server-Erweiterung auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="b9f81-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="b9f81-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9f81-104">SYNTAX</span></span>

```
Get-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9f81-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9f81-105">DESCRIPTION</span></span>
<span data-ttu-id="b9f81-106">Das Cmdlet " **Get-AzVMSqlServerExtension** " Ruft die Einstellungen des SQL Server Infrastructure as a Service (IaaS)-Agents auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="b9f81-106">The **Get-AzVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="b9f81-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9f81-107">EXAMPLES</span></span>

### <span data-ttu-id="b9f81-108">Beispiel 1: Abrufen der Einstellungen einer SQL Server-Erweiterung auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="b9f81-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
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

<span data-ttu-id="b9f81-109">Dieser Befehl ruft die Einstellungen der SQL Server-Erweiterung auf einem virtuellen Computer mit dem Namen ContosoVM07 ab.</span><span class="sxs-lookup"><span data-stu-id="b9f81-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="b9f81-110">Beispiel 2: Abrufen der Einstellungen mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="b9f81-110">Example 2: Get the settings by using the pipeline</span></span>
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

<span data-ttu-id="b9f81-111">Dieser Befehl ruft den virtuellen Computer mit dem Namen ContosoVM22 auf dem Dienst Service08 mithilfe des Get-AzVM-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="b9f81-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="b9f81-112">Der Befehl übergibt die Ergebnisse mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9f81-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b9f81-113">Der aktuelle Befehl ruft die Einstellungen des SQL Server-IaaS-Agents auf dem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="b9f81-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="b9f81-114">Beispiel 3: Abrufen der Einstellungen einer bestimmten SQL Server-Version</span><span class="sxs-lookup"><span data-stu-id="b9f81-114">Example 3: Get the settings of specific SQL Server version</span></span>
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

<span data-ttu-id="b9f81-115">Dieser Befehl ruft die Einstellungen von Version 1,0 der SQL Server-Erweiterung auf einem virtuellen Computer mit dem Namen ContosoVM07 ab.</span><span class="sxs-lookup"><span data-stu-id="b9f81-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="b9f81-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9f81-116">PARAMETERS</span></span>

### <span data-ttu-id="b9f81-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9f81-117">-DefaultProfile</span></span>
<span data-ttu-id="b9f81-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b9f81-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9f81-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b9f81-119">-Name</span></span>
<span data-ttu-id="b9f81-120">Gibt den Namen der SQL Server-Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="b9f81-120">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="b9f81-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9f81-121">-ResourceGroupName</span></span>
<span data-ttu-id="b9f81-122">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="b9f81-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b9f81-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="b9f81-123">-VMName</span></span>
<span data-ttu-id="b9f81-124">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="b9f81-124">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="b9f81-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9f81-125">CommonParameters</span></span>
<span data-ttu-id="b9f81-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9f81-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9f81-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9f81-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9f81-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b9f81-128">INPUTS</span></span>

### <span data-ttu-id="b9f81-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b9f81-129">System.String</span></span>

## <span data-ttu-id="b9f81-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b9f81-130">OUTPUTS</span></span>

### <span data-ttu-id="b9f81-131">Microsoft. Azure. Commands. Compute. VirtualMachineSqlServerExtensionContext</span><span class="sxs-lookup"><span data-stu-id="b9f81-131">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span></span>

## <span data-ttu-id="b9f81-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="b9f81-132">NOTES</span></span>

## <span data-ttu-id="b9f81-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b9f81-133">RELATED LINKS</span></span>

[<span data-ttu-id="b9f81-134">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="b9f81-134">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="b9f81-135">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b9f81-135">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="b9f81-136">Satz-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b9f81-136">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


