---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: 70da17c175c49da80cf4ee5ed71509aa98db99b6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845855"
---
# <span data-ttu-id="ca8d5-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="ca8d5-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="ca8d5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ca8d5-102">SYNOPSIS</span></span>
<span data-ttu-id="ca8d5-103">Löscht die Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ca8d5-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="ca8d5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca8d5-104">SYNTAX</span></span>

### <span data-ttu-id="ca8d5-105">ObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ca8d5-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca8d5-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca8d5-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca8d5-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca8d5-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca8d5-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca8d5-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca8d5-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca8d5-109">DESCRIPTION</span></span>
<span data-ttu-id="ca8d5-110">Löscht die Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ca8d5-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="ca8d5-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ca8d5-111">EXAMPLES</span></span>

### <span data-ttu-id="ca8d5-112">Beispiel 1: Entfernen der Anwendung nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="ca8d5-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="ca8d5-113">Entfernt die Anwendung mit der Objekt-ID "b4cd1619-80b3-4cfb-9f8f-9f2333425738" aus dem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="ca8d5-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="ca8d5-114">Beispiel 2 – Entfernen der Anwendung nach Anwendungs-ID</span><span class="sxs-lookup"><span data-stu-id="ca8d5-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="ca8d5-115">Entfernt die Anwendung mit der Anwendungs-ID "f9c5ea4f-28f0-401a-A491-491a037fa346" aus dem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="ca8d5-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="ca8d5-116">Beispiel 3 – Entfernen der Anwendung durch Verrohrung</span><span class="sxs-lookup"><span data-stu-id="ca8d5-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="ca8d5-117">Ruft die Anwendung mit der Objekt-ID "b4cd1619-80b3-4cfb-9f8f-9f2333425738" und Pipes ab, die zum Cmdlet Remove-AzADApplication, um die Anwendung aus dem Mandanten zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="ca8d5-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="ca8d5-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca8d5-118">PARAMETERS</span></span>

### <span data-ttu-id="ca8d5-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ca8d5-119">-ApplicationId</span></span>
<span data-ttu-id="ca8d5-120">Die Anwendungs-ID der zu entfernenden Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ca8d5-120">The application id of the application to remove.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca8d5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca8d5-121">-DefaultProfile</span></span>
<span data-ttu-id="ca8d5-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ca8d5-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca8d5-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ca8d5-123">-DisplayName</span></span>
<span data-ttu-id="ca8d5-124">Der Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ca8d5-124">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca8d5-125">-Force</span><span class="sxs-lookup"><span data-stu-id="ca8d5-125">-Force</span></span>
<span data-ttu-id="ca8d5-126">Wechseln Sie, um eine Anwendung ohne Bestätigung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="ca8d5-126">Switch to delete an application without a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8d5-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ca8d5-127">-InputObject</span></span>
<span data-ttu-id="ca8d5-128">Das Objekt, das die zu entfernende Anwendung darstellt.</span><span class="sxs-lookup"><span data-stu-id="ca8d5-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca8d5-129">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="ca8d5-129">-ObjectId</span></span>
<span data-ttu-id="ca8d5-130">Die Objekt-ID der zu löschenden Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ca8d5-130">The object id of the application to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca8d5-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca8d5-131">-PassThru</span></span>
<span data-ttu-id="ca8d5-132">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="ca8d5-132">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8d5-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ca8d5-133">-Confirm</span></span>
<span data-ttu-id="ca8d5-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ca8d5-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8d5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca8d5-135">-WhatIf</span></span>
<span data-ttu-id="ca8d5-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca8d5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca8d5-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ca8d5-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8d5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca8d5-138">CommonParameters</span></span>
<span data-ttu-id="ca8d5-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca8d5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca8d5-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca8d5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca8d5-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ca8d5-141">INPUTS</span></span>

### <span data-ttu-id="ca8d5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ca8d5-142">System.String</span></span>

### <span data-ttu-id="ca8d5-143">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ca8d5-143">System.Guid</span></span>

### <span data-ttu-id="ca8d5-144">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="ca8d5-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="ca8d5-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ca8d5-145">OUTPUTS</span></span>

### <span data-ttu-id="ca8d5-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ca8d5-146">System.Boolean</span></span>

## <span data-ttu-id="ca8d5-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="ca8d5-147">NOTES</span></span>
<span data-ttu-id="ca8d5-148">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="ca8d5-148">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="ca8d5-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ca8d5-149">RELATED LINKS</span></span>

[<span data-ttu-id="ca8d5-150">Neu – AzADApplication</span><span class="sxs-lookup"><span data-stu-id="ca8d5-150">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="ca8d5-151">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="ca8d5-151">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="ca8d5-152">Satz-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="ca8d5-152">Set-AzADApplication</span></span>](./Set-AzADApplication.md)

[<span data-ttu-id="ca8d5-153">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ca8d5-153">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

