---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5312556cb49d02ea901b4cb2526a36f7237f66d1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404172"
---
# <span data-ttu-id="51300-101">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="51300-101">New-AzureSqlDatabaseServerContext</span></span>

## <span data-ttu-id="51300-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51300-102">SYNOPSIS</span></span>
<span data-ttu-id="51300-103">Erstellt einen Serververbindungskontext.</span><span class="sxs-lookup"><span data-stu-id="51300-103">Creates a server connection context.</span></span>

## <span data-ttu-id="51300-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51300-104">SYNTAX</span></span>

### <span data-ttu-id="51300-105">ByServerNameWithSqlAuth (Standard)</span><span class="sxs-lookup"><span data-stu-id="51300-105">ByServerNameWithSqlAuth (Default)</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="51300-106">ByManageUrlWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="51300-106">ByManageUrlWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="51300-107">ByServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="51300-107">ByServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="51300-108">ByFullyQualifiedServerNameWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="51300-108">ByFullyQualifiedServerNameWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="51300-109">ByFullyQualifiedServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="51300-109">ByFullyQualifiedServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="51300-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51300-110">DESCRIPTION</span></span>
<span data-ttu-id="51300-111">Das **Cmdlet "New-AzureSqlDatabaseServerContext"** erstellt einen Azure SQL Datenbankserververbindungskontext.</span><span class="sxs-lookup"><span data-stu-id="51300-111">The **New-AzureSqlDatabaseServerContext** cmdlet creates an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="51300-112">Verwenden SQL Server A0 zum Erstellen eines Verbindungskontexts mit SQL Datenbankserver mit den angegebenen Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="51300-112">Use SQL Server authentication to create a connection context to a SQL Database server by using the specified credentials.</span></span>
<span data-ttu-id="51300-113">Sie können den SQL Datenbankserver nach Name, vollqualifizierten Namen oder URL angeben.</span><span class="sxs-lookup"><span data-stu-id="51300-113">You can specify the SQL Database server by name, by the fully qualified name, or by URL.</span></span>
<span data-ttu-id="51300-114">Zum Abrufen von Anmeldeinformationen verwenden Sie das Get-Credential-Cmdlet, in dem Sie aufgefordert werden, den Benutzernamen und das Kennwort anzugeben.</span><span class="sxs-lookup"><span data-stu-id="51300-114">To obtain a credential, use the Get-Credential cmdlet that prompts you to specify the user name and password.</span></span>

<span data-ttu-id="51300-115">Verwenden Sie **das Cmdlet "New-AzureSqlDatabaseServerContext"** mit zertifikatbasierter Authentifizierung, um einen Verbindungskontext mit dem angegebenen SQL-Datenbankserver mithilfe der angegebenen Azure-Abonnementdaten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="51300-115">Use the **New-AzureSqlDatabaseServerContext** cmdlet with certificate based authentication to create a connection context to the specified SQL Database server by using the specified Azure subscription data.</span></span>
<span data-ttu-id="51300-116">Sie können SQL Datenbankserver nach Name oder nach dem vollqualifizierten Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="51300-116">You can specify SQL Database server by name or by the fully qualified name.</span></span>
<span data-ttu-id="51300-117">Sie können die Abonnementdaten als Parameter angeben oder sie aus dem aktuellen Abonnement von Azure abrufen.</span><span class="sxs-lookup"><span data-stu-id="51300-117">You can specify the subscription data as a parameter or it can be retrieved from the current Azure subscription.</span></span>
<span data-ttu-id="51300-118">Verwenden Sie das Cmdlet "Select-AzureSubscription", https://msdn.microsoft.com/library/windowsazure/jj152833.aspx um das aktuelle Azure-Abonnement auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="51300-118">Use the Select-AzureSubscriptionhttps://msdn.microsoft.com/library/windowsazure/jj152833.aspx cmdlet to select the current Azure subscription.</span></span>

## <span data-ttu-id="51300-119">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="51300-119">EXAMPLES</span></span>

### <span data-ttu-id="51300-120">Beispiel 1: Erstellen eines Kontexts mithilfe SQL Server Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="51300-120">Example 1: Create a context by using SQL Server authentication</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="51300-121">In diesem Beispiel wird die SQL Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="51300-121">This example uses the SQL Server authentication.</span></span>

<span data-ttu-id="51300-122">Der erste Befehl fordert Sie zur Eingabe von Serveradministratoranmeldeinformationen auf und speichert die Anmeldeinformationen in der $Credential Variable.</span><span class="sxs-lookup"><span data-stu-id="51300-122">The first command prompts you for server administrator credentials, and stores the credentials in the $Credential variable.</span></span>

<span data-ttu-id="51300-123">Der zweite Befehl stellt mithilfe von "lpqd0zbr8y" eine Verbindung mit dem SQL Datenbankserver $Credential.</span><span class="sxs-lookup"><span data-stu-id="51300-123">The second command connects to the SQL Database server named lpqd0zbr8y by using $Credential.</span></span>

<span data-ttu-id="51300-124">Mit dem letzten Befehl wird eine Datenbank mit dem Namen "Database17" auf dem Server erstellt, die Teil des Kontexts in $Context.</span><span class="sxs-lookup"><span data-stu-id="51300-124">The final command creates a database named Database17 on the server that is part of the context in $Context.</span></span>

### <span data-ttu-id="51300-125">Beispiel 2: Erstellen eines Kontexts mithilfe der zertifikatbasierten Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="51300-125">Example 2: Create a context by using certificate based authentication</span></span>
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

<span data-ttu-id="51300-126">In diesem Beispiel wird die zertifikatbasierte Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="51300-126">This example uses the certificate based authentication.</span></span>

<span data-ttu-id="51300-127">Die ersten beiden Befehle weisen den Variablen $SubscriptionId $Thumbprint zu.</span><span class="sxs-lookup"><span data-stu-id="51300-127">The first two commands assign values to the $SubscriptionId and $Thumbprint variables.</span></span>

<span data-ttu-id="51300-128">Der dritte Befehl ruft das Zertifikat ab, das durch den Fingerabdruck in der $Thumbprint identifiziert wurde, und speichert es in $Certificate.</span><span class="sxs-lookup"><span data-stu-id="51300-128">The third command gets the certificate identified by the thumbprint in $Thumbprint, and stores it in $Certificate.</span></span>

<span data-ttu-id="51300-129">Der vierte Befehl legt das Abonnement auf "Subscription07" fest, und mit dem fünften Befehl wird dieses Abonnement ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="51300-129">The fourth command sets the subscription to be Subscription07, and the fifth command selects that subscription.</span></span>

<span data-ttu-id="51300-130">Der letzte Befehl erstellt einen Kontext im aktuellen Abonnement für den Server namens lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="51300-130">The final command creates a context in the current subscription for the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="51300-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51300-131">PARAMETERS</span></span>

### <span data-ttu-id="51300-132">-Credential</span><span class="sxs-lookup"><span data-stu-id="51300-132">-Credential</span></span>
<span data-ttu-id="51300-133">Gibt ein Anmeldeinformationsobjekt an, das SQL Server für den Zugriff auf den Server bietet.</span><span class="sxs-lookup"><span data-stu-id="51300-133">Specifies a credential object that provides SQL Server authentication for you to access the server.</span></span>

```yaml
Type: PSCredential
Parameter Sets: ByServerNameWithSqlAuth, ByManageUrlWithSqlAuth, ByFullyQualifiedServerNameWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51300-134">-FullyQualifiedServerName</span><span class="sxs-lookup"><span data-stu-id="51300-134">-FullyQualifiedServerName</span></span>
<span data-ttu-id="51300-135">Gibt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) für den Azure SQL Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="51300-135">Specifies the fully qualified domain name (FQDN) name for the Azure SQL Database server.</span></span>
<span data-ttu-id="51300-136">Beispiel: Server02.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="51300-136">For example, Server02.database.windows.net.</span></span>

```yaml
Type: String
Parameter Sets: ByFullyQualifiedServerNameWithSqlAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51300-137">-ManageUrl</span><span class="sxs-lookup"><span data-stu-id="51300-137">-ManageUrl</span></span>
<span data-ttu-id="51300-138">Gibt die URL an, die dieses Cmdlet für den Zugriff auf das Azure SQL DatabaseManagement Portal für den Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="51300-138">Specifies the URL that this cmdlet uses to access the Azure SQL DatabaseManagement Portal for the server.</span></span>

```yaml
Type: Uri
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51300-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="51300-139">-Profile</span></span>
<span data-ttu-id="51300-140">Gibt das Azure-Profil an, aus dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="51300-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="51300-141">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="51300-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="51300-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="51300-142">-ServerName</span></span>
<span data-ttu-id="51300-143">Gibt den Namen des Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="51300-143">Specifies the name of the database server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameWithSqlAuth, ByServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51300-144">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="51300-144">-SubscriptionName</span></span>
<span data-ttu-id="51300-145">Gibt den Namen des Azure-Abonnements an, das von diesem Cmdlet zum Erstellen des Verbindungskontexts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="51300-145">Specifies the name of the Azure subscription that this cmdlet uses to create the connection context.</span></span>
<span data-ttu-id="51300-146">Wenn Sie keinen Wert für diesen Parameter angeben, verwendet das Cmdlet das aktuelle Abonnement.</span><span class="sxs-lookup"><span data-stu-id="51300-146">If you do not specify a value for this parameter, the cmdlet uses the current subscription.</span></span>
<span data-ttu-id="51300-147">Führen Sie Select-AzureSubscription cmdlet aus, um das aktuelle Abonnement zu ändern.</span><span class="sxs-lookup"><span data-stu-id="51300-147">Run the Select-AzureSubscription cmdlet to change the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51300-148">-UseSubscription</span><span class="sxs-lookup"><span data-stu-id="51300-148">-UseSubscription</span></span>
<span data-ttu-id="51300-149">Gibt an, dass dieses Cmdlet das Abonnement von Azure zum Erstellen des Verbindungskontexts verwendet.</span><span class="sxs-lookup"><span data-stu-id="51300-149">Indicates that this cmdlet uses Azure subscription for creating the connection context.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51300-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51300-150">CommonParameters</span></span>
<span data-ttu-id="51300-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51300-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51300-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51300-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51300-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="51300-153">INPUTS</span></span>

## <span data-ttu-id="51300-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="51300-154">OUTPUTS</span></span>

### <span data-ttu-id="51300-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext</span><span class="sxs-lookup"><span data-stu-id="51300-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext</span></span>

## <span data-ttu-id="51300-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="51300-156">NOTES</span></span>
* <span data-ttu-id="51300-157">Wenn Sie sich authentifizieren, ohne eine Domäne anzugeben, und wenn Sie Windows PowerShell 2.0 verwenden, gibt das Cmdlet Get-Credential einen umgekehrten Schrägstrich () zurück, der dem Benutzernamen vorankommt, z. B. \\ "\user".</span><span class="sxs-lookup"><span data-stu-id="51300-157">If you authenticate without specifying a domain, and if you use Windows PowerShell 2.0, the Get-Credential cmdlet returns a backslash (\\) prepended to the username, for example, \user.</span></span> <span data-ttu-id="51300-158">Windows PowerShell 3.0 wird kein umgekehrter Schrägstrich hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="51300-158">Windows PowerShell 3.0 does not add the backslash.</span></span> <span data-ttu-id="51300-159">Dieser umgekehrte Schrägstrich wird vom Parameter *"Credential"* des **Cmdlets "New-AzureSqlDatabaseServerContext"** nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="51300-159">This backslash is not recognized by the *Credential* parameter of the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span> <span data-ttu-id="51300-160">Verwenden Sie zum Entfernen Befehle wie die folgenden:</span><span class="sxs-lookup"><span data-stu-id="51300-160">To remove it, use commands similar to the following:</span></span>

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## <span data-ttu-id="51300-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="51300-161">RELATED LINKS</span></span>



[<span data-ttu-id="51300-162">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="51300-162">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="51300-163">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="51300-163">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="51300-164">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="51300-164">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="51300-165">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="51300-165">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


