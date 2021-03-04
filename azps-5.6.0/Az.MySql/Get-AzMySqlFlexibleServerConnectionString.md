---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserverconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConnectionString.md
ms.openlocfilehash: a1f5c89b33ad4d547907bd63427a45ef262518c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948592"
---
# <span data-ttu-id="07f85-101">Get-AzMySqlFlexibleServerConnectionString</span><span class="sxs-lookup"><span data-stu-id="07f85-101">Get-AzMySqlFlexibleServerConnectionString</span></span>

## <span data-ttu-id="07f85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07f85-102">SYNOPSIS</span></span>
<span data-ttu-id="07f85-103">Holen Sie sich die Verbindungszeichenfolge entsprechend dem Clientverbindungsanbieter.</span><span class="sxs-lookup"><span data-stu-id="07f85-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="07f85-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07f85-104">SYNTAX</span></span>

### <span data-ttu-id="07f85-105">Get (Standard)</span><span class="sxs-lookup"><span data-stu-id="07f85-105">Get (Default)</span></span>
```
Get-AzMySqlFlexibleServerConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="07f85-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="07f85-106">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerConnectionString -Client <String> -InputObject <IMySqlIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="07f85-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07f85-107">DESCRIPTION</span></span>
<span data-ttu-id="07f85-108">Holen Sie sich die Verbindungszeichenfolge entsprechend dem Clientverbindungsanbieter.</span><span class="sxs-lookup"><span data-stu-id="07f85-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="07f85-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="07f85-109">EXAMPLES</span></span>

### <span data-ttu-id="07f85-110">Beispiel 1: Verbindungszeichenfolge nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="07f85-110">Example 1: Get connection string by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConnectionString -Client Python -ResourceGroupName PowershellMySqlTest -Name mysql-test

cnx = mysql.connector.connect(user=mysql_user, password="{your_password}", host="mysql-test.mysql.database.azure.com", port=3306, database="{your_database}", ssl_ca="{ca-cert filename}", ssl_disabled=False)
```

<span data-ttu-id="07f85-111">Dieses Cmdlet zeigt die Verbindungszeichenfolge eines Clients nach Servername an.</span><span class="sxs-lookup"><span data-stu-id="07f85-111">This cmdlet shows connection string of a client by server name.</span></span>

### <span data-ttu-id="07f85-112">Beispiel 2: Get MySql server connection string by identity</span><span class="sxs-lookup"><span data-stu-id="07f85-112">Example 2: Get MySql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlFlexibleServerConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="07f85-113">Dieses Cmdlet ruft die MySql-Serververbindungszeichenfolge nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="07f85-113">This cmdlet gets MySql server connection string by identity.</span></span>

## <span data-ttu-id="07f85-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="07f85-114">PARAMETERS</span></span>

### <span data-ttu-id="07f85-115">-Client</span><span class="sxs-lookup"><span data-stu-id="07f85-115">-Client</span></span>
<span data-ttu-id="07f85-116">Clientverbindungsanbieter.</span><span class="sxs-lookup"><span data-stu-id="07f85-116">Client connection provider.</span></span>

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

### <span data-ttu-id="07f85-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f85-117">-DefaultProfile</span></span>
<span data-ttu-id="07f85-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07f85-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07f85-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07f85-119">-InputObject</span></span>
<span data-ttu-id="07f85-120">Der Server für die Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="07f85-120">The server for the connection string.</span></span>
<span data-ttu-id="07f85-121">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="07f85-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07f85-122">-Name</span><span class="sxs-lookup"><span data-stu-id="07f85-122">-Name</span></span>
<span data-ttu-id="07f85-123">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="07f85-123">The name of the server.</span></span>

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

### <span data-ttu-id="07f85-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07f85-124">-ResourceGroupName</span></span>
<span data-ttu-id="07f85-125">Der Name der Ressourcengruppe, die die Ressource enthält. Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="07f85-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07f85-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="07f85-126">-SubscriptionId</span></span>
<span data-ttu-id="07f85-127">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="07f85-127">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07f85-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f85-128">CommonParameters</span></span>
<span data-ttu-id="07f85-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07f85-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f85-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07f85-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f85-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="07f85-131">INPUTS</span></span>

### <span data-ttu-id="07f85-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="07f85-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="07f85-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="07f85-133">OUTPUTS</span></span>

### <span data-ttu-id="07f85-134">System.String</span><span class="sxs-lookup"><span data-stu-id="07f85-134">System.String</span></span>

## <span data-ttu-id="07f85-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="07f85-135">NOTES</span></span>

<span data-ttu-id="07f85-136">ALIASE</span><span class="sxs-lookup"><span data-stu-id="07f85-136">ALIASES</span></span>

<span data-ttu-id="07f85-137">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="07f85-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="07f85-138">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="07f85-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="07f85-139">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="07f85-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="07f85-140">INPUTOBJECT <IMySqlIdentity> : Der Server für die Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="07f85-140">INPUTOBJECT <IMySqlIdentity>: The server for the connection string.</span></span>
  - <span data-ttu-id="07f85-141">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="07f85-141">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="07f85-142">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="07f85-142">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="07f85-143">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="07f85-143">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="07f85-144">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="07f85-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="07f85-145">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="07f85-145">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="07f85-146">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="07f85-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="07f85-147">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="07f85-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="07f85-148">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="07f85-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="07f85-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="07f85-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="07f85-150">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="07f85-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="07f85-151">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="07f85-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="07f85-152">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="07f85-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="07f85-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="07f85-153">RELATED LINKS</span></span>

