---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
ms.openlocfilehash: f7d6dab2629dc8247cb404d1de2dc58b21fc8a2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502322"
---
# <span data-ttu-id="6f6ab-101">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="6f6ab-101">Set-AzureRmSqlServer</span></span>

## <span data-ttu-id="6f6ab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6f6ab-102">SYNOPSIS</span></span>
<span data-ttu-id="6f6ab-103">Ändert die Eigenschaften eines SQL-Datenbankservers.</span><span class="sxs-lookup"><span data-stu-id="6f6ab-103">Modifies properties of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f6ab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f6ab-104">SYNTAX</span></span>

```
Set-AzureRmSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f6ab-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f6ab-105">DESCRIPTION</span></span>
<span data-ttu-id="6f6ab-106">Das Cmdlet " **Satz-AzureRmSqlServer** " ändert die Eigenschaften eines Azure SQL-Datenbankservers.</span><span class="sxs-lookup"><span data-stu-id="6f6ab-106">The **Set-AzureRmSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="6f6ab-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f6ab-107">EXAMPLES</span></span>

### <span data-ttu-id="6f6ab-108">Beispiel 1: Zurücksetzen des Administratorkennworts</span><span class="sxs-lookup"><span data-stu-id="6f6ab-108">Example 1: Reset the administrator password</span></span>
```
PS C:\>$ServerPassword = "newpassword"
PS C:\> $SecureString = ConvertTo-SecureString $ServerPassword -AsPlainText -Force
PS C:\> Set-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SqlAdministratorPassword $secureString
ResourceGroupName        : ResourceGroup01
ServerName               : Server01
Location                 : Australia East
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="6f6ab-109">Mit diesem Befehl wird das Administratorkennwort auf dem AzureSQL-Server mit dem Namen Server01 zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="6f6ab-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="6f6ab-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f6ab-110">PARAMETERS</span></span>

### <span data-ttu-id="6f6ab-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="6f6ab-111">-AssignIdentity</span></span>
<span data-ttu-id="6f6ab-112">Sie können eine Azure Active Directory-Identität für diesen Server für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault generieren und zuweisen.</span><span class="sxs-lookup"><span data-stu-id="6f6ab-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f6ab-113">-DefaultProfile</span></span>
<span data-ttu-id="6f6ab-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6f6ab-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6ab-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6f6ab-115">-Force</span></span>
<span data-ttu-id="6f6ab-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="6f6ab-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6ab-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f6ab-117">-ResourceGroupName</span></span>
<span data-ttu-id="6f6ab-118">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="6f6ab-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="6f6ab-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="6f6ab-119">-ServerName</span></span>
<span data-ttu-id="6f6ab-120">Gibt den Namen des Servers an, der vom Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="6f6ab-120">Specifies the name of the server that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f6ab-121">-Server Version vom</span><span class="sxs-lookup"><span data-stu-id="6f6ab-121">-ServerVersion</span></span>
<span data-ttu-id="6f6ab-122">Gibt die Version an, für die dieses Cmdlet den Server ändert.</span><span class="sxs-lookup"><span data-stu-id="6f6ab-122">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="6f6ab-123">Die zulässigen Werte für diesen Parameter lauten: 2,0 und 12,0.</span><span class="sxs-lookup"><span data-stu-id="6f6ab-123">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6ab-124">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="6f6ab-124">-SqlAdministratorPassword</span></span>
<span data-ttu-id="6f6ab-125">Gibt ein neues Kennwort als **SecureString** für den Datenbankserver-Administrator an.</span><span class="sxs-lookup"><span data-stu-id="6f6ab-125">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="6f6ab-126">Verwenden Sie das Get-Credential-Cmdlet, um eine **SecureString** -Anwendung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6f6ab-126">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="6f6ab-127">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="6f6ab-127">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6ab-128">-Tags</span><span class="sxs-lookup"><span data-stu-id="6f6ab-128">-Tags</span></span>
<span data-ttu-id="6f6ab-129">Gibt ein Wörterbuch mit Tags an, die dieses Cmdlet dem Server anordnet.</span><span class="sxs-lookup"><span data-stu-id="6f6ab-129">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="6f6ab-130">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server definiert ist.</span><span class="sxs-lookup"><span data-stu-id="6f6ab-130">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="6f6ab-131">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="6f6ab-131">For example:</span></span>

<span data-ttu-id="6f6ab-132">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="6f6ab-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6ab-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6f6ab-133">-Confirm</span></span>
<span data-ttu-id="6f6ab-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6f6ab-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6ab-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f6ab-135">-WhatIf</span></span>
<span data-ttu-id="6f6ab-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6f6ab-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f6ab-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f6ab-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6ab-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f6ab-138">CommonParameters</span></span>
<span data-ttu-id="6f6ab-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f6ab-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f6ab-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f6ab-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f6ab-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6f6ab-141">INPUTS</span></span>

### <span data-ttu-id="6f6ab-142">Keine</span><span class="sxs-lookup"><span data-stu-id="6f6ab-142">None</span></span>
<span data-ttu-id="6f6ab-143">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="6f6ab-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6f6ab-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6f6ab-144">OUTPUTS</span></span>

### <span data-ttu-id="6f6ab-145">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="6f6ab-145">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="6f6ab-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="6f6ab-146">NOTES</span></span>

## <span data-ttu-id="6f6ab-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6f6ab-147">RELATED LINKS</span></span>

[<span data-ttu-id="6f6ab-148">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="6f6ab-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
