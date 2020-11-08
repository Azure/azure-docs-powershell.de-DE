---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
ms.openlocfilehash: 43af6a438a36df5360fd062aaf22e85e95fa62a1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174657"
---
# <span data-ttu-id="089b9-101">Get-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="089b9-101">Get-AzMariaDbServer</span></span>

## <span data-ttu-id="089b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="089b9-102">SYNOPSIS</span></span>
<span data-ttu-id="089b9-103">Ruft Informationen zu einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="089b9-103">Gets information about a server.</span></span>

## <span data-ttu-id="089b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="089b9-104">SYNTAX</span></span>

### <span data-ttu-id="089b9-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="089b9-105">List1 (Default)</span></span>
```
Get-AzMariaDbServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="089b9-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="089b9-106">Get</span></span>
```
Get-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="089b9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="089b9-107">GetViaIdentity</span></span>
```
Get-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="089b9-108">Liste</span><span class="sxs-lookup"><span data-stu-id="089b9-108">List</span></span>
```
Get-AzMariaDbServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="089b9-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="089b9-109">DESCRIPTION</span></span>
<span data-ttu-id="089b9-110">Ruft Informationen zu einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="089b9-110">Gets information about a server.</span></span>

## <span data-ttu-id="089b9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="089b9-111">EXAMPLES</span></span>

### <span data-ttu-id="089b9-112">Beispiel 1: Auflisten aller MariaDB unter Abonnements</span><span class="sxs-lookup"><span data-stu-id="089b9-112">Example 1: List all MariaDB under a subscriptions</span></span>
```powershell
PS C:\> Get-AzMariaDbServer

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName    SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------    -------        --------------
mrdb01                     eastus   dolauli            10.2    5120                    B_Gen5_1   Basic          Enabled
wyunchi-10                 eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
wyunchi                    eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
wyunchi-eastus             eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-h3pame        eastus   qiszomtkpf         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-4rmtig        eastus   xofavpndqj         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-szp6dt        eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-9pebvn        eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-asd-01             eastus   adminuser          10.2    5120                    B_Gen5_1   Basic          Enabled
rst-001                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rst-002                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-003           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-004           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
```

<span data-ttu-id="089b9-113">Dieser Befehl listet alle MariaDB unter Abonnements auf.</span><span class="sxs-lookup"><span data-stu-id="089b9-113">This command lists all MariaDB under a subscriptions.</span></span>

### <span data-ttu-id="089b9-114">Beispiel 2: Auflisten aller MariaDB unter einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="089b9-114">Example 2: List all MariaDB under a resource group</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName    SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------    -------        --------------
mariadb-test-h3pame        eastus   qiszomtkpf         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-4rmtig        eastus   xofavpndqj         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-szp6dt        eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-9pebvn        eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-asd-01             eastus   adminuser          10.2    5120                    B_Gen5_1   Basic          Enabled
rst-001                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rst-002                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-003           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-004           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
```

<span data-ttu-id="089b9-115">Dieser Befehl listet alle MariaDB unter einer Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="089b9-115">This command lists all MariaDB under a resource group.</span></span>

### <span data-ttu-id="089b9-116">Beispiel 3: Abrufen eines MariaDB</span><span class="sxs-lookup"><span data-stu-id="089b9-116">Example 3: Get a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0 -Name mariadb-test-h3pame

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-h3pame eastus   qiszomtkpf         10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="089b9-117">Dieser Befehl ruft eine MariaDB ab.</span><span class="sxs-lookup"><span data-stu-id="089b9-117">This command gets a MariaDB.</span></span>

## <span data-ttu-id="089b9-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="089b9-118">PARAMETERS</span></span>

### <span data-ttu-id="089b9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="089b9-119">-DefaultProfile</span></span>
<span data-ttu-id="089b9-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="089b9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="089b9-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="089b9-121">-InputObject</span></span>
<span data-ttu-id="089b9-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="089b9-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="089b9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="089b9-123">-Name</span></span>
<span data-ttu-id="089b9-124">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="089b9-124">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="089b9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="089b9-125">-ResourceGroupName</span></span>
<span data-ttu-id="089b9-126">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="089b9-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="089b9-127">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="089b9-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="089b9-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="089b9-128">-SubscriptionId</span></span>
<span data-ttu-id="089b9-129">Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="089b9-129">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="089b9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="089b9-130">CommonParameters</span></span>
<span data-ttu-id="089b9-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="089b9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="089b9-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="089b9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="089b9-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="089b9-133">INPUTS</span></span>

### <span data-ttu-id="089b9-134">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="089b9-134">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="089b9-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="089b9-135">OUTPUTS</span></span>

### <span data-ttu-id="089b9-136">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="089b9-136">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="089b9-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="089b9-137">NOTES</span></span>

<span data-ttu-id="089b9-138">Aliase</span><span class="sxs-lookup"><span data-stu-id="089b9-138">ALIASES</span></span>

<span data-ttu-id="089b9-139">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="089b9-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="089b9-140">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="089b9-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="089b9-141">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="089b9-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="089b9-142">Inputobject <IMariaDbIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="089b9-142">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="089b9-143">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="089b9-143">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="089b9-144">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="089b9-144">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="089b9-145">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="089b9-145">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="089b9-146">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="089b9-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="089b9-147">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="089b9-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="089b9-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="089b9-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="089b9-149">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="089b9-149">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="089b9-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="089b9-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="089b9-151">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="089b9-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="089b9-152">`[SubscriptionId <String>]`: Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="089b9-152">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="089b9-153">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="089b9-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="089b9-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="089b9-154">RELATED LINKS</span></span>

