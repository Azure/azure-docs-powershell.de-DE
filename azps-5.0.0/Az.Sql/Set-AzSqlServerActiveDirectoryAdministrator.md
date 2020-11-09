---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: d450fa7795a530106a72180210d9cb133c7d3047
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300460"
---
# <span data-ttu-id="c07c2-101">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c07c2-101">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="c07c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c07c2-102">SYNOPSIS</span></span>
<span data-ttu-id="c07c2-103">Stellt einen Azure AD-Administrator für SQL Server vor.</span><span class="sxs-lookup"><span data-stu-id="c07c2-103">Provisions an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="c07c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c07c2-104">SYNTAX</span></span>

```
Set-AzSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c07c2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c07c2-105">DESCRIPTION</span></span>
<span data-ttu-id="c07c2-106">Das Cmdlet " **Satz-AzSqlServerActiveDirectoryAdministrator" stellt** einen Azure Active Directory (Azure AD)-Administrator für den AzureSQL-Server im aktuellen Abonnement dar.</span><span class="sxs-lookup"><span data-stu-id="c07c2-106">The **Set-AzSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>
<span data-ttu-id="c07c2-107">Sie können jeweils nur einen Administrator bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c07c2-107">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="c07c2-108">Die folgenden Mitglieder von Azure AD können als SQL Server-Administrator bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="c07c2-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>
- <span data-ttu-id="c07c2-109">Native Member von Azure AD</span><span class="sxs-lookup"><span data-stu-id="c07c2-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="c07c2-110">Verbundmitglieder von Azure AD</span><span class="sxs-lookup"><span data-stu-id="c07c2-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="c07c2-111">Importierte Mitglieder aus anderen Azure ADS, die native oder Federated-Mitglieder sind</span><span class="sxs-lookup"><span data-stu-id="c07c2-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="c07c2-112">Azure AD Groups, die als Sicherheitsgruppen von Microsoft-Konten erstellt wurden, wie beispielsweise die in der Outlook.com-, hotmail.com-oder Live.com-Domäne, werden nicht als Administratoren unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c07c2-112">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="c07c2-113">Andere Gastkonten, beispielsweise die in der gmail.com-oder Yahoo.com-Domäne, werden nicht als Administratoren unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c07c2-113">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="c07c2-114">Wir empfehlen, dass Sie eine dedizierte Azure Ad-Gruppe als Administrator bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c07c2-114">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="c07c2-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c07c2-115">EXAMPLES</span></span>

### <span data-ttu-id="c07c2-116">Beispiel 1: Bereitstelleneiner Administratorgruppe für einen Server</span><span class="sxs-lookup"><span data-stu-id="c07c2-116">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- ---------------------------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="c07c2-117">Dieser Befehl stellt eine Azure AD-Administratorgruppe namens DBAs für den Server mit dem Namen Server01 dar.</span><span class="sxs-lookup"><span data-stu-id="c07c2-117">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="c07c2-118">Dieser Server ist dem Ressourcengruppen-ResourceGroup01 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c07c2-118">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="c07c2-119">Beispiel 2: Bereitstellen eines Administratorbenutzers für einen Server</span><span class="sxs-lookup"><span data-stu-id="c07c2-119">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9 False
```

<span data-ttu-id="c07c2-120">Mit diesem Befehl wird ein Azure AD-Benutzer als Administrator für den Server mit dem Namen "Server01" abgeregelt.</span><span class="sxs-lookup"><span data-stu-id="c07c2-120">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="c07c2-121">Beispiel 3: Bereitstelleneiner Administratorgruppe durch Angabe der ID</span><span class="sxs-lookup"><span data-stu-id="c07c2-121">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="c07c2-122">Dieser Befehl stellt eine Azure AD-Administratorgruppe namens DBAs für den Server mit dem Namen Server01 dar.</span><span class="sxs-lookup"><span data-stu-id="c07c2-122">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="c07c2-123">Der Befehl gibt eine ID für den *objectID* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="c07c2-123">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="c07c2-124">Dadurch wird sichergestellt, dass der Befehl erfolgreich ausgeführt wird, auch wenn der Anzeigename der Gruppe nicht eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="c07c2-124">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="c07c2-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="c07c2-125">PARAMETERS</span></span>

### <span data-ttu-id="c07c2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c07c2-126">-DefaultProfile</span></span>
<span data-ttu-id="c07c2-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c07c2-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c07c2-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c07c2-128">-DisplayName</span></span>
<span data-ttu-id="c07c2-129">Gibt den Anzeigenamen des Azure AD-Administrators an, der von diesem Cmdlet vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="c07c2-129">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c07c2-130">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="c07c2-130">-ObjectId</span></span>
<span data-ttu-id="c07c2-131">Gibt die eindeutige ID des Azure AD-Administrators an, der von diesem Cmdlet abgeregelt wird.</span><span class="sxs-lookup"><span data-stu-id="c07c2-131">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="c07c2-132">Wenn der Anzeigename nicht eindeutig ist, müssen Sie einen Wert für diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="c07c2-132">If the display name is not unique, you must specify a value for this parameter.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c07c2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c07c2-133">-ResourceGroupName</span></span>
<span data-ttu-id="c07c2-134">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c07c2-134">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="c07c2-135">-Servername</span><span class="sxs-lookup"><span data-stu-id="c07c2-135">-ServerName</span></span>
<span data-ttu-id="c07c2-136">Gibt den Namen des SQL-Servers an, für den ein Administrator von diesem Cmdlet vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="c07c2-136">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

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

### <span data-ttu-id="c07c2-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c07c2-137">-Confirm</span></span>
<span data-ttu-id="c07c2-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c07c2-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07c2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c07c2-139">-WhatIf</span></span>
<span data-ttu-id="c07c2-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c07c2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c07c2-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c07c2-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07c2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c07c2-142">CommonParameters</span></span>
<span data-ttu-id="c07c2-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c07c2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c07c2-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c07c2-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c07c2-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c07c2-145">INPUTS</span></span>

### <span data-ttu-id="c07c2-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c07c2-146">System.String</span></span>

### <span data-ttu-id="c07c2-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c07c2-147">System.Guid</span></span>

## <span data-ttu-id="c07c2-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c07c2-148">OUTPUTS</span></span>

### <span data-ttu-id="c07c2-149">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="c07c2-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="c07c2-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="c07c2-150">NOTES</span></span>

## <span data-ttu-id="c07c2-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c07c2-151">RELATED LINKS</span></span>

[<span data-ttu-id="c07c2-152">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c07c2-152">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="c07c2-153">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c07c2-153">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="c07c2-154">Deaktivieren-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="c07c2-154">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="c07c2-155">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="c07c2-155">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


