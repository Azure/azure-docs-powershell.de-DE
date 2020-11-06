---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: a6f2ed82835cca252f905cb53c5ddd9c8530900a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503858"
---
# <span data-ttu-id="f6e23-101">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="f6e23-101">Get-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="f6e23-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f6e23-102">SYNOPSIS</span></span>
<span data-ttu-id="f6e23-103">Ruft die Einstellungen für eine SQL Server-Erweiterung auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="f6e23-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6e23-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6e23-104">SYNTAX</span></span>

```
Get-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6e23-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6e23-105">DESCRIPTION</span></span>
<span data-ttu-id="f6e23-106">Das Cmdlet " **Get-AzureRmVMSqlServerExtension** " Ruft die Einstellungen des SQL Server Infrastructure as a Service (IaaS)-Agents auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="f6e23-106">The **Get-AzureRmVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="f6e23-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f6e23-107">EXAMPLES</span></span>

### <span data-ttu-id="f6e23-108">Beispiel 1: Abrufen der Einstellungen einer SQL Server-Erweiterung auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="f6e23-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="f6e23-109">Dieser Befehl ruft die Einstellungen der SQL Server-Erweiterung auf einem virtuellen Computer mit dem Namen ContosoVM07 ab.</span><span class="sxs-lookup"><span data-stu-id="f6e23-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="f6e23-110">Beispiel 2: Abrufen der Einstellungen mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="f6e23-110">Example 2: Get the settings by using the pipeline</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service08" -Name "ContosoVM22" | Get-AzureRmVMSqlServerExtension
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="f6e23-111">Dieser Befehl ruft den virtuellen Computer mit dem Namen ContosoVM22 auf dem Dienst Service08 mithilfe des Get-AzureRmVM-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="f6e23-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="f6e23-112">Der Befehl übergibt die Ergebnisse mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6e23-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="f6e23-113">Der aktuelle Befehl ruft die Einstellungen des SQL Server-IaaS-Agents auf dem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="f6e23-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="f6e23-114">Beispiel 3: Abrufen der Einstellungen einer bestimmten SQL Server-Version</span><span class="sxs-lookup"><span data-stu-id="f6e23-114">Example 3: Get the settings of specific SQL Server version</span></span>
```
PS C:\> Get-AzureRmVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07" -Version "1.0"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="f6e23-115">Dieser Befehl ruft die Einstellungen von Version 1,0 der SQL Server-Erweiterung auf einem virtuellen Computer mit dem Namen ContosoVM07 ab.</span><span class="sxs-lookup"><span data-stu-id="f6e23-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="f6e23-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6e23-116">PARAMETERS</span></span>

### <span data-ttu-id="f6e23-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f6e23-117">-Name</span></span>
<span data-ttu-id="f6e23-118">Gibt den Namen der SQL Server-Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="f6e23-118">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6e23-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6e23-119">-ResourceGroupName</span></span>
<span data-ttu-id="f6e23-120">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="f6e23-120">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6e23-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="f6e23-121">-VMName</span></span>
<span data-ttu-id="f6e23-122">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="f6e23-122">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6e23-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6e23-123">CommonParameters</span></span>
<span data-ttu-id="f6e23-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6e23-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6e23-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6e23-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6e23-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f6e23-126">INPUTS</span></span>

### <span data-ttu-id="f6e23-127">Keine</span><span class="sxs-lookup"><span data-stu-id="f6e23-127">None</span></span>
<span data-ttu-id="f6e23-128">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f6e23-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f6e23-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f6e23-129">OUTPUTS</span></span>

## <span data-ttu-id="f6e23-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="f6e23-130">NOTES</span></span>

## <span data-ttu-id="f6e23-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f6e23-131">RELATED LINKS</span></span>

[<span data-ttu-id="f6e23-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f6e23-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="f6e23-133">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="f6e23-133">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="f6e23-134">Satz-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="f6e23-134">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


