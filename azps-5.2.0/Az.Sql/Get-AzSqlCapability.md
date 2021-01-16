---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 8C5D29AD-0B15-4CD4-8637-86ABD19F41C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
ms.openlocfilehash: 582b512ef502e0dac3fc443807f1e33a65063728
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299936"
---
# <span data-ttu-id="dc97d-101">Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="dc97d-101">Get-AzSqlCapability</span></span>

## <span data-ttu-id="dc97d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc97d-102">SYNOPSIS</span></span>
<span data-ttu-id="dc97d-103">Ruft SQL Datenbankfunktionen für das aktuelle Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="dc97d-103">Gets SQL Database capabilities for the current subscription.</span></span>

## <span data-ttu-id="dc97d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc97d-104">SYNTAX</span></span>

### <span data-ttu-id="dc97d-105">FilterResults (Standard)</span><span class="sxs-lookup"><span data-stu-id="dc97d-105">FilterResults (Default)</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-ServerVersionName <String>] [-EditionName <String>]
 [-ServiceObjectiveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc97d-106">DefaultResults</span><span class="sxs-lookup"><span data-stu-id="dc97d-106">DefaultResults</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-Defaults] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc97d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc97d-107">DESCRIPTION</span></span>
<span data-ttu-id="dc97d-108">Das **Cmdlet "Get-AzSqlCapability"** ruft die Azure SQL-Datenbankfunktionen ab, die im aktuellen Abonnement für eine Region verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="dc97d-108">The **Get-AzSqlCapability** cmdlet gets the Azure SQL Database capabilities available on the current subscription for a region.</span></span>
<span data-ttu-id="dc97d-109">Wenn Sie die Parameter *"ServerVersionName",* *"EditionName"* oder *"ServiceObjectiveName"* angeben, gibt dieses Cmdlet die angegebenen Werte und ihre Vorgänger zurück.</span><span class="sxs-lookup"><span data-stu-id="dc97d-109">If you specify the *ServerVersionName*, *EditionName*, or *ServiceObjectiveName* parameters, this cmdlet returns the specified values and their predecessors.</span></span>

## <span data-ttu-id="dc97d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dc97d-110">EXAMPLES</span></span>

### <span data-ttu-id="dc97d-111">Beispiel 1: Erhalten von Funktionen für das aktuelle Abonnement für eine Region</span><span class="sxs-lookup"><span data-stu-id="dc97d-111">Example 1: Get capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US"
Location                : Central US
Status                  : Available
SupportedServerVersions : {12.0, 2.0}
```

<span data-ttu-id="dc97d-112">Dieser Befehl gibt die Funktionen für SQL Datenbankinstanzen im aktuellen Abonnement für die Region "USA, Mitte" zurück.</span><span class="sxs-lookup"><span data-stu-id="dc97d-112">This command returns the capabilities for SQL Database instances on the current subscription for the Central US region.</span></span>

### <span data-ttu-id="dc97d-113">Beispiel 2: Erhalten von Standardfunktionen für das aktuelle Abonnement für eine Region</span><span class="sxs-lookup"><span data-stu-id="dc97d-113">Example 2: Get default capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -Defaults
Location        : Central US
Status          : Available
ExpandedDetails : Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S0 (Default)
```

<span data-ttu-id="dc97d-114">Dieser Befehl gibt die Standardfunktionen für SQL Datenbanken für das aktuelle Abonnement in der Region "USA, Mitte" zurück.</span><span class="sxs-lookup"><span data-stu-id="dc97d-114">This command returns the default capabilities for SQL Databases on the current subscription in the Central US region.</span></span>

### <span data-ttu-id="dc97d-115">Beispiel 3: Anzeigen von Details für ein Dienstziel</span><span class="sxs-lookup"><span data-stu-id="dc97d-115">Example 3: Get details for a service objective</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -ServiceObjectiveName "S1"
Location        : Central US
Status          : Available
ExpandedDetails : Version: 12.0 (Available) -> Edition: Standard (Default) -> Service Objective: S1 (Available) 
                  Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S1 (Available)
```

<span data-ttu-id="dc97d-116">Dieser Befehl ruft Standardfunktionen für SQL für das angegebene Dienstziel im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="dc97d-116">This command gets default capabilities for SQL Databases for the specified service objective on the current subscription.</span></span>

## <span data-ttu-id="dc97d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc97d-117">PARAMETERS</span></span>

### <span data-ttu-id="dc97d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc97d-118">-DefaultProfile</span></span>
<span data-ttu-id="dc97d-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="dc97d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc97d-120">-Standardwerte</span><span class="sxs-lookup"><span data-stu-id="dc97d-120">-Defaults</span></span>
<span data-ttu-id="dc97d-121">Gibt an, dass dieses Cmdlet nur Standardwerte erhält.</span><span class="sxs-lookup"><span data-stu-id="dc97d-121">Indicates that this cmdlet gets only defaults.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc97d-122">-EditionName</span><span class="sxs-lookup"><span data-stu-id="dc97d-122">-EditionName</span></span>
<span data-ttu-id="dc97d-123">Gibt den Namen der Datenbankedition an, für die dieses Cmdlet Funktionen erhält.</span><span class="sxs-lookup"><span data-stu-id="dc97d-123">Specifies the name of the database edition for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc97d-124">-LocationName</span><span class="sxs-lookup"><span data-stu-id="dc97d-124">-LocationName</span></span>
<span data-ttu-id="dc97d-125">Gibt den Namen des Speicherorts an, für den dieses Cmdlet Funktionen erhält.</span><span class="sxs-lookup"><span data-stu-id="dc97d-125">Specifies the name of the Location for which this cmdlet gets capabilities.</span></span>
<span data-ttu-id="dc97d-126">Weitere Informationen finden Sie unter "Azure-Regionen http://azure.microsoft.com/en-us/regions/ ( http://azure.microsoft.com/en-us/regions/) .</span><span class="sxs-lookup"><span data-stu-id="dc97d-126">For more information, see Azure Regionshttp://azure.microsoft.com/en-us/regions/ (http://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="dc97d-127">-ServerVersionName</span><span class="sxs-lookup"><span data-stu-id="dc97d-127">-ServerVersionName</span></span>
<span data-ttu-id="dc97d-128">Gibt den Namen der Serverversion an, für die dieses Cmdlet Funktionen erhält.</span><span class="sxs-lookup"><span data-stu-id="dc97d-128">Specifies the name of the server version for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc97d-129">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="dc97d-129">-ServiceObjectiveName</span></span>
<span data-ttu-id="dc97d-130">Gibt den Namen des Dienstziels an, für das dieses Cmdlet Funktionen erhält.</span><span class="sxs-lookup"><span data-stu-id="dc97d-130">Specifies the name of the service objective for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc97d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc97d-131">-Confirm</span></span>
<span data-ttu-id="dc97d-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dc97d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc97d-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="dc97d-133">-WhatIf</span></span>
<span data-ttu-id="dc97d-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc97d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc97d-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dc97d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc97d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc97d-136">CommonParameters</span></span>
<span data-ttu-id="dc97d-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc97d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc97d-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc97d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc97d-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dc97d-139">INPUTS</span></span>

### <span data-ttu-id="dc97d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="dc97d-140">System.String</span></span>

## <span data-ttu-id="dc97d-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dc97d-141">OUTPUTS</span></span>

### <span data-ttu-id="dc97d-142">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span><span class="sxs-lookup"><span data-stu-id="dc97d-142">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span></span>

## <span data-ttu-id="dc97d-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dc97d-143">NOTES</span></span>

## <span data-ttu-id="dc97d-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dc97d-144">RELATED LINKS</span></span>
