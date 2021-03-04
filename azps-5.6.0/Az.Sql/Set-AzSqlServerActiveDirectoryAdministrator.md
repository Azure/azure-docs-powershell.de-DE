---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 37fe534b13226f81c7639275a3c35f3a54d3543b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933384"
---
# <span data-ttu-id="c7913-101">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c7913-101">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="c7913-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7913-102">SYNOPSIS</span></span>
<span data-ttu-id="c7913-103">Bietet einen Azure AD-Administrator für SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c7913-103">Provisions an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="c7913-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7913-104">SYNTAX</span></span>

```
Set-AzSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c7913-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7913-105">DESCRIPTION</span></span>
<span data-ttu-id="c7913-106">Das **Cmdlet Set-AzSqlServerActiveDirectoryAdministrator** stellt einen Azure Active Directory (Azure AD)-Administrator für AzureSQL Server im aktuellen Abonnement bereit.</span><span class="sxs-lookup"><span data-stu-id="c7913-106">The **Set-AzSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>
<span data-ttu-id="c7913-107">Sie können immer nur einen Administrator gleichzeitig bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c7913-107">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="c7913-108">Die folgenden Mitglieder von Azure AD können als Administrator SQL Server werden:</span><span class="sxs-lookup"><span data-stu-id="c7913-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>
- <span data-ttu-id="c7913-109">Native Mitglieder von Azure AD</span><span class="sxs-lookup"><span data-stu-id="c7913-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="c7913-110">Verbundmitglieder von Azure AD</span><span class="sxs-lookup"><span data-stu-id="c7913-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="c7913-111">Importierte Mitglieder aus anderen Azure ADs, die native Oder Verbundmitglieder sind</span><span class="sxs-lookup"><span data-stu-id="c7913-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="c7913-112">Azure AD-Gruppen, die als Sicherheitsgruppen von Microsoft-Konten erstellt wurden, z. B. in Outlook.com-, Hotmail.com- oder Live.com-Domänen, werden als Administratoren nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c7913-112">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="c7913-113">Andere Gastkonten, z. B. in den domänen Gmail.com oder Yahoo.com, werden als Administratoren nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c7913-113">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="c7913-114">Es wird empfohlen, eine dedizierte Azure AD-Gruppe als Administrator bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c7913-114">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="c7913-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c7913-115">EXAMPLES</span></span>

### <span data-ttu-id="c7913-116">Beispiel 1: Bereitstellen einer Administratorgruppe für einen Server</span><span class="sxs-lookup"><span data-stu-id="c7913-116">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- ---------------------------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="c7913-117">Dieser Befehl enthält eine Azure AD-Administratorgruppe mit dem Namen DBAs für den Server mit dem Namen Server01.</span><span class="sxs-lookup"><span data-stu-id="c7913-117">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="c7913-118">Dieser Server ist der Ressourcengruppe ResourceGroup01 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c7913-118">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="c7913-119">Beispiel 2: Bereitstellen eines Administratorbenutzers für einen Server</span><span class="sxs-lookup"><span data-stu-id="c7913-119">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9 False
```

<span data-ttu-id="c7913-120">Dieser Befehl enthält einen Azure AD-Benutzer als Administrator für den Server mit dem Namen Server01.</span><span class="sxs-lookup"><span data-stu-id="c7913-120">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="c7913-121">Beispiel 3: Bereitstellen einer Administratorgruppe durch Angeben der ID</span><span class="sxs-lookup"><span data-stu-id="c7913-121">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="c7913-122">Dieser Befehl enthält eine Azure AD-Administratorgruppe mit dem Namen DBAs für den Server mit dem Namen Server01.</span><span class="sxs-lookup"><span data-stu-id="c7913-122">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="c7913-123">Der Befehl gibt eine ID für den *Parameter ObjectId* an.</span><span class="sxs-lookup"><span data-stu-id="c7913-123">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="c7913-124">Dadurch wird sichergestellt, dass der Befehl auch dann erfolgreich ist, wenn der Anzeigename der Gruppe nicht eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="c7913-124">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="c7913-125">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c7913-125">PARAMETERS</span></span>

### <span data-ttu-id="c7913-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7913-126">-DefaultProfile</span></span>
<span data-ttu-id="c7913-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c7913-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7913-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c7913-128">-DisplayName</span></span>
<span data-ttu-id="c7913-129">Gibt den Anzeigenamen des Azure AD-Administrators an, den dieses Cmdlet vorgibt.</span><span class="sxs-lookup"><span data-stu-id="c7913-129">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

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

### <span data-ttu-id="c7913-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c7913-130">-ObjectId</span></span>
<span data-ttu-id="c7913-131">Gibt die eindeutige ID des Azure AD-Administrators an, die von diesem Cmdlet bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c7913-131">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="c7913-132">Wenn der Anzeigename nicht eindeutig ist, müssen Sie einen Wert für diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="c7913-132">If the display name is not unique, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="c7913-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7913-133">-ResourceGroupName</span></span>
<span data-ttu-id="c7913-134">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c7913-134">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="c7913-135">-Servername</span><span class="sxs-lookup"><span data-stu-id="c7913-135">-ServerName</span></span>
<span data-ttu-id="c7913-136">Gibt den Namen der SQL Server an, für die dieses Cmdlet einen Administrator enthält.</span><span class="sxs-lookup"><span data-stu-id="c7913-136">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

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

### <span data-ttu-id="c7913-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c7913-137">-Confirm</span></span>
<span data-ttu-id="c7913-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c7913-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7913-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7913-139">-WhatIf</span></span>
<span data-ttu-id="c7913-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c7913-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7913-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7913-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7913-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7913-142">CommonParameters</span></span>
<span data-ttu-id="c7913-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7913-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7913-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7913-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7913-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c7913-145">INPUTS</span></span>

### <span data-ttu-id="c7913-146">System.String</span><span class="sxs-lookup"><span data-stu-id="c7913-146">System.String</span></span>

### <span data-ttu-id="c7913-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="c7913-147">System.Guid</span></span>

## <span data-ttu-id="c7913-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c7913-148">OUTPUTS</span></span>

### <span data-ttu-id="c7913-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="c7913-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="c7913-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c7913-150">NOTES</span></span>

## <span data-ttu-id="c7913-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c7913-151">RELATED LINKS</span></span>

[<span data-ttu-id="c7913-152">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c7913-152">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="c7913-153">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c7913-153">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="c7913-154">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="c7913-154">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="c7913-155">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="c7913-155">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


