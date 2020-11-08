---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8CE8F4E9-93D4-41E5-8B43-F886C018D9FB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06681544df4974a1ee906552af96302698e88d74
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005736"
---
# <span data-ttu-id="e1a2e-101">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e1a2e-101">Get-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="e1a2e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1a2e-102">SYNOPSIS</span></span>
<span data-ttu-id="e1a2e-103">Ruft die Einstellungen des SQL Server-IaaS-Agents auf einem bestimmten virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="e1a2e-103">Gets the settings of the SQL Server IaaS Agent on a particular virtual machine.</span></span>

## <span data-ttu-id="e1a2e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1a2e-104">SYNTAX</span></span>

```
Get-AzureVMSqlServerExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e1a2e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1a2e-105">DESCRIPTION</span></span>
<span data-ttu-id="e1a2e-106">Das Cmdlet " **Get-AzureVMSqlServerExtension** " Ruft die Einstellungen des SQL Server Infrastructure as a Service (IaaS)-Agents auf einem bestimmten virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="e1a2e-106">The **Get-AzureVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a particular virtual machine.</span></span>

## <span data-ttu-id="e1a2e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1a2e-107">EXAMPLES</span></span>

### <span data-ttu-id="e1a2e-108">Beispiel 1: Abrufen der Einstellungen einer SQL Server-Erweiterung auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="e1a2e-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVMSqlServerExtension-VM $VM
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="e1a2e-109">Ruft die Einstellungen der SQL Server-Erweiterung auf einem bestimmten virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="e1a2e-109">Gets the settings of the SQL Server extension on a particular virtual machine.</span></span>

### <span data-ttu-id="e1a2e-110">Beispiel 2: Abrufen der Einstellungen eines SQL Server-IaaS-Agents auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="e1a2e-110">Example 2: Get the settings of a SQL Server IaaS Agent on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Get-AzureVMSqlServerExtension
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="e1a2e-111">Ruft die Einstellungen des SQL Server-IaaS-Agents auf einem bestimmten virtuellen Computer mithilfe von piped Input ab.</span><span class="sxs-lookup"><span data-stu-id="e1a2e-111">Gets the settings of the SQL Server IaaS Agent on a particular virtual machine using piped input.</span></span>

### <span data-ttu-id="e1a2e-112">Beispiel 3: Abrufen der Einstellungen eines bestimmten SQL Server-Versions IaaS-Agents auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="e1a2e-112">Example 3: Get the settings of specific SQL Server version IaaS Agent on a virtual machine</span></span>
```
PS C:\> Get-AzureVMSqlServerExtension -VM $VM -Version "1.0"
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="e1a2e-113">Dieser Befehl ruft die Einstellungen der jeweiligen Version des SQL Server-IaaS-Agents auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="e1a2e-113">This command gets the settings of the particular version of SQL Server IaaS Agent on a virtual machine.</span></span>

## <span data-ttu-id="e1a2e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1a2e-114">PARAMETERS</span></span>

### <span data-ttu-id="e1a2e-115">-Information</span><span class="sxs-lookup"><span data-stu-id="e1a2e-115">-InformationAction</span></span>
<span data-ttu-id="e1a2e-116">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="e1a2e-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e1a2e-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e1a2e-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e1a2e-118">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="e1a2e-118">Continue</span></span>
- <span data-ttu-id="e1a2e-119">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="e1a2e-119">Ignore</span></span>
- <span data-ttu-id="e1a2e-120">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="e1a2e-120">Inquire</span></span>
- <span data-ttu-id="e1a2e-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e1a2e-121">SilentlyContinue</span></span>
- <span data-ttu-id="e1a2e-122">Beenden</span><span class="sxs-lookup"><span data-stu-id="e1a2e-122">Stop</span></span>
- <span data-ttu-id="e1a2e-123">Anhalten</span><span class="sxs-lookup"><span data-stu-id="e1a2e-123">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1a2e-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e1a2e-124">-InformationVariable</span></span>
<span data-ttu-id="e1a2e-125">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="e1a2e-125">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1a2e-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="e1a2e-126">-Profile</span></span>
<span data-ttu-id="e1a2e-127">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="e1a2e-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e1a2e-128">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="e1a2e-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e1a2e-129">-VM</span><span class="sxs-lookup"><span data-stu-id="e1a2e-129">-VM</span></span>
<span data-ttu-id="e1a2e-130">Gibt das Objekt des beständigen virtuellen Computers an, von dem dieses Cmdlet Einstellungen erhält.</span><span class="sxs-lookup"><span data-stu-id="e1a2e-130">Specifies the persistent virtual machine object that this cmdlet gets settings from.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1a2e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1a2e-131">CommonParameters</span></span>
<span data-ttu-id="e1a2e-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1a2e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1a2e-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1a2e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1a2e-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1a2e-134">INPUTS</span></span>

## <span data-ttu-id="e1a2e-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1a2e-135">OUTPUTS</span></span>

## <span data-ttu-id="e1a2e-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1a2e-136">NOTES</span></span>

## <span data-ttu-id="e1a2e-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1a2e-137">RELATED LINKS</span></span>

[<span data-ttu-id="e1a2e-138">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e1a2e-138">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)

[<span data-ttu-id="e1a2e-139">Satz-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e1a2e-139">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


